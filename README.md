# AI Content API

Fast, affordable AI text generation for builders and content teams: summarize, rewrite, fix grammar, and generate product descriptions, titles and SEO meta descriptions — all from one simple REST API.

**Live on RapidAPI:** https://rapidapi.com/cesaricf79/api/ai-content-api

Free tier included. Get your key and ready-to-paste snippets (curl, Python, Node) on the listing above.

## Why

Most AI text APIs bill per token and get expensive fast. This one runs on open LLMs we host ourselves, so the pricing stays low and predictable — the same generations at a fraction of the cost. Send text, get clean text back. No SDK, no streaming setup.

## Endpoints

- **POST /v1/ai/summarize** — condense any text to N sentences.
- **POST /v1/ai/rewrite** — rewrite in a chosen tone (professional, casual, friendly, persuasive, formal, simple).
- **POST /v1/ai/improve** — fix grammar, spelling and clarity, keeping the meaning.
- **POST /v1/ai/product-description** — e-commerce product copy from a name + features.
- **POST /v1/ai/titles** — catchy / SEO / YouTube titles and headlines.
- **POST /v1/ai/meta-description** — an SEO meta description under 155 characters.

Every endpoint accepts `"quality": true` to switch from the fast model to a higher-quality (slower) one.

## Typical uses

- Bulk-generate product descriptions for online stores.
- Summarize articles, tickets, reviews or transcripts.
- Clean up and rewrite user-generated or draft text.
- Produce titles and meta descriptions for blogs and SEO at scale.

## Example

```bash
curl -X POST "https://.../v1/ai/product-description" \
  -H "Content-Type: application/json" \
  -d '{"name":"Wireless Noise-Cancelling Headphones","features":"40h battery, Bluetooth 5.3, memory foam cushions, USB-C","words":55}'
```

```json
{ "description": "Experience ultimate comfort and clarity ...", "model": "llama3.2:3b" }
```

## Notes

- Simple JSON in, JSON out. No async jobs to poll.
- Input is capped per request to keep latency predictable.
- Designed to be cheap to run at scale — that's why the pricing is low.

Full request/response examples and per-language code are on the RapidAPI listing.

## License

Client examples: MIT. The hosted API is provided via RapidAPI.
