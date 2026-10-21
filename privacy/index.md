---
title: Privacy Policy
permalink: /privacy/
---

# Letrino Privacy Policy

_Effective date: October 20, 2026_

Letrino is a Chrome extension for learning languages from song lyrics. This policy explains what data Letrino handles, where it goes, and what stays on your device.

**In short:** Letrino has no servers and collects nothing. By default, all explanations and translations are generated on your device. Lyrics leave your device only if you add your own Anthropic API key and choose "Annotate with Claude". Even then they go to Anthropic under your account, never to us.

## What Letrino reads

On Genius lyrics pages (`genius.com`), Letrino reads the song's lyrics and the words or phrases you select. It uses them to detect the song's language, translate lines, and explain your selection in context. Letrino does not run on any other website.

## What Letrino stores

All storage uses Chrome's extension storage. Nothing is stored on servers run by the developer.

- **Settings:** your native language, your proficiency levels, per-song language corrections, and the songs where you turned on whole-song translation (identified by their Genius page address). These are kept in `chrome.storage.sync`. If Chrome sync is on, Chrome syncs them across your signed-in browsers through your Google account, under [Google's privacy policy](https://policies.google.com/privacy).
- **Optional Anthropic API key and Claude preferences:** if you add a key, it is kept only on this device, in `chrome.storage.local`. Access is restricted to Letrino's own extension pages and service worker: it is never exposed to web pages and never synced. You can remove it at any time in the Letrino popup.
- **Model status:** whether the on-device language model has finished downloading.

Uninstalling Letrino deletes all of its stored data from your browser.

## On-device AI (the default)

Explanations are generated on your device by Chrome's built-in AI (the Prompt API). For languages it doesn't support, they come from an on-device model run with WebLLM. Translations use Chrome's built-in Translator API, also on your device. With these, lyrics and selections never leave your device.

Models are downloaded once and then run locally:

- **Chrome's built-in models** (for explanations and translation) are downloaded and managed by Chrome itself.
- **The WebLLM model** (about 1.8 GB, used only for languages Chrome's AI doesn't support) is downloaded from Hugging Face (`huggingface.co`) and cached by your browser.

These downloads fetch model files only. No lyrics, selections, settings, or other personal data are sent with them.

## Optional: Claude annotations (your own API key)

If you save an Anthropic API key, Letrino offers an "Annotate with Claude" button after the on-device explanation. Before the first request, Letrino asks for your consent to send lyrics to Anthropic. After you agree, each time you click the button:

- the selected text, the song's lyrics as context, the song's language, your native language and proficiency level are sent directly from your browser to Anthropic's API (`api.anthropic.com`), authenticated with your key;
- if you enabled web search, Claude may search the web for slang or idioms in the selection, and the response includes the sources it used.

Requests go under your own Anthropic account and are billed to it. Anthropic handles them under its own terms and privacy policy ([anthropic.com/legal/privacy](https://www.anthropic.com/legal/privacy)). Nothing is sent to Anthropic unless you click the button.

## What Letrino does not do

- No analytics, telemetry, tracking, or advertising.
- No data is sent to the developer. Letrino has no developer-run servers.
- No data is sold or shared, and no data is used for anything other than Letrino's language-learning features.
- No access to pages other than Genius lyrics pages.

## Changes to this policy

If Letrino's data handling changes, this policy will be updated and the effective date above will change.

## Contact

Questions about this policy: [taylorbarmak@gmail.com](mailto:taylorbarmak@gmail.com)
