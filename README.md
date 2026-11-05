# Deslop - LLM Voice Detector

A [Pollinations](https://pollinations.ai) prompt agent about the way language models write, built for quest [#19180](https://github.com/pollinations/pollinations/issues/19180).

Paste AI-sounding text and Deslop:

1. **Voice report** - lists the LLM-voice tics it found, with quoted evidence: inflated vocabulary (delve, pivotal, seamless), stock filler ("in today's fast-paced world"), structural tics (rule-of-three, "not just X, but Y", synonym cycling), superficial -ing phrases ("highlighting the significance"), em-dash overuse and false depth - then scores HUMAN-LIKENESS x/100.
2. **Rewrite** - the same text in a plain human voice. Every fact, name, number and claim is kept; filler is cut, not replaced.
3. **Notes** - what changed and why.

## Use it

- **Model:** `community/Dcode9/deslop`
- **Base model:** `anthropic/claude-haiku-4.5`
- **Config:** [agent.json](agent.json)

Call it with your own Pollinations key - you pay with your own Pollen:

```bash
curl https://gen.pollinations.ai/v1/chat/completions \
  -H "Authorization: Bearer YOUR_POLLINATIONS_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "community/Dcode9/deslop",
    "messages": [{"role": "user", "content": "PASTE TEXT HERE"}]
  }'
```

Or open it in [Open WebUI](https://openwebui.pollinations.ai/?model=community%2FDcode9%2Fdeslop).

Inspired by Martin Fowler's [LLM Voice](https://martinfowler.com/bliki/LLM-Voice.html) and [training the AI writing tics out of a small model](https://100toolkit.com/blog/deslop-model/).

[![Made with pollinations.ai](https://raw.githubusercontent.com/pollinations/pollinations/main/packages/ui/src/brand/badge-made-with.svg)](https://pollinations.ai/?ref=badge)
