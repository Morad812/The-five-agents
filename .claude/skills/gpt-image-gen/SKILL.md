---
name: gpt-image-gen
description: "Generate images via OpenAI Images API (gpt-image-2). Accepts a prompt and output path, returns the saved PNG. Used by any agent that needs image generation."
---

# gpt-image-gen — OpenAI Image Generation

Generate a PNG image from a text prompt using OpenAI's image generation API.

## Prerequisites

`OPENAI_API_KEY` must be set in `.env` at the project root.

## Usage

Caller provides:
- `PROMPT` — full image prompt string
- `OUTPUT_PATH` — destination path for the PNG (e.g. `yuval/outputs/2026-05-06-hero-banner.png`)

## Execution

### Step 1 — Load API key

Read `OPENAI_API_KEY` from `.env`:

```bash
export OPENAI_API_KEY=$(grep '^OPENAI_API_KEY=' .env | cut -d'=' -f2-)
```

Abort with a clear error if the key is empty:

```bash
if [ -z "$OPENAI_API_KEY" ]; then
  echo "❌ OPENAI_API_KEY not set in .env — cannot generate image"
  exit 1
fi
```

### Step 2 — Call the API

```bash
curl -s -X POST "https://api.openai.com/v1/images/generations" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d "{
    \"model\": \"gpt-image-2\",
    \"prompt\": \"$PROMPT\",
    \"size\": \"1024x1024\",
    \"quality\": \"medium\",
    \"output_format\": \"png\"
  }" > /tmp/openai_image_response.json
```

### Step 3 — Decode base64 to PNG

**jq (preferred, if available):**
```bash
jq -r '.data[0].b64_json' /tmp/openai_image_response.json | base64 --decode > "$OUTPUT_PATH"
```

**Python fallback (Git Bash / environments without jq):**
```bash
python3 -c "
import json, base64
data = json.load(open('/tmp/openai_image_response.json'))
b64 = data['data'][0]['b64_json']
open('$OUTPUT_PATH', 'wb').write(base64.b64decode(b64))
"
```

**Auto-detect approach:**
```bash
if command -v jq &>/dev/null; then
  jq -r '.data[0].b64_json' /tmp/openai_image_response.json | base64 --decode > "$OUTPUT_PATH"
else
  python3 -c "
import json, base64
data = json.load(open('/tmp/openai_image_response.json'))
open('$OUTPUT_PATH', 'wb').write(base64.b64decode(data['data'][0]['b64_json']))
"
fi
```

### Step 4 — Validate

```bash
[ -s "$OUTPUT_PATH" ] && echo "✅ Image saved: $OUTPUT_PATH" || echo "❌ Output file is empty or missing"
```

## Error Handling

- If `data[0].b64_json` is absent, the API returned an error — print the full response JSON to diagnose.
- **HTTP 401**: API key is invalid or not set.
- **HTTP 400**: Prompt was rejected (policy violation) — rephrase and retry.
- **Empty file after decode**: Check that `base64 --decode` / Python write succeeded without errors.
