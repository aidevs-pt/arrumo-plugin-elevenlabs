# Arrumo ElevenLabs Plugin

The default ElevenLabs adapter for transcription and audio generation.

Copyright © 2026 DEVS AI Unipessoal LDA. Licensed under the [GNU Affero General Public License v3.0](LICENSE).

For custom AI solutions for your company, visit [DEVS AI](https://aidevs.pt).

The bundled transcription adapter uses `transcription.json` to declare its endpoint, model, and SDK credential field. Arrumo handles the WAV upload and resolves the credential from its system store. See [ElevenLabs' transcription API reference](https://elevenlabs.io/docs/api-reference/speech-to-text/convert).

The SDK speech synthesis descriptor in `speech-synthesis.json` maps the
workspace credential and caller-supplied voice ID to the ElevenLabs
[Create speech endpoint](https://elevenlabs.io/docs/api-reference/text-to-speech/convert).
It requests MP3 from the Multilingual v2 model and caps each request at
2,500 characters per request. Use the Arrumo host speech commands for dispatch.
Arrumo narrates storyboarded videos with the workspace's **Voice ID** setting,
or with the George voice (`JBFqnCBsd6RMkjVDRZzb`) when it is empty.

## Transcription and subtitles

[English](docs/en/transcription.md) · [Español](docs/es/transcription.md) · [Português](docs/pt/transcription.md)

## Package a release candidate

From this checkout, use the Arrumo Plugin SDK packager with the adapter files
listed explicitly. Record the SDK commit and the SHA-256 printed by the tool.

```sh
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include speech-synthesis.json
```
