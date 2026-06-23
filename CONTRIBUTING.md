# Contributing

Thanks for thinking about contributing — this project is meant to be forked, tweaked, and improved. Contributions of **every size** are welcome, including a one-line typo fix or "this part confused me."

## The project in 30 seconds

It's a **single file**: `index.html`. HTML, CSS, and JavaScript all live there — no build step, no dependencies, no framework. Open it in a browser and it runs. That's the whole architecture.

- **Styling** lives in CSS variables at the top of the `<style>` block.
- **AI calls** go through `callLLM()`, which routes to `callOpenAI()` or `callAnthropic()`.
- **Voice** is handled by Deepgram (WebSocket) or the browser's `SpeechRecognition`, with text-to-speech via `speechSynthesis`.

## How to contribute

1. **Fork** the repo and clone your fork.
2. Open `index.html` in your browser and make changes — refresh to see them.
3. Test with **both** an OpenAI key and a Claude key if you touched the AI layer.
4. Open a **pull request** describing what you changed and why. Screenshots or a short clip help a lot for UI changes.

No PR is too small. If you're not ready to write code, **open an issue** — bug reports, ideas, and "I got stuck here" notes are all valuable.

## Good first contributions

- Add another AI provider (Gemini, Mistral, Ollama for local models).
- Add an optional backend proxy so API keys never live in the browser.
- Support non-English interviews.
- Export the session summary as a PDF.
- Persist scores across sessions to chart improvement.
- Accessibility passes (keyboard nav, ARIA, screen-reader testing).

## Ground rules

- Keep it **dependency-free and single-file** unless there's a strong reason not to — that simplicity is the point.
- Don't add analytics, trackers, or anything that sends user data anywhere except the AI provider the user chose.
- Be kind in reviews and issues. Assume good intent.

That's it. Happy hacking.
