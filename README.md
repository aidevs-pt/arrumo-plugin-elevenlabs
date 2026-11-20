# Arrumo ElevenLabs Plugin

The default ElevenLabs adapter for transcription and audio generation.

This repository is being initialized. See the Arrumo workspace roadmap for implementation status.

Copyright © 2026 DEVS AI Unipessoal LDA. Licensed under the [GNU Affero General Public License v3.0](LICENSE).

For custom AI solutions for your company, visit [DEVS AI](https://aidevs.pt).

The bundled transcription adapter uses `transcription.json` to declare its endpoint, model, and SDK credential field. Arrumo handles the WAV upload and resolves the credential from its system store. See [ElevenLabs' transcription API reference](https://elevenlabs.io/docs/api-reference/speech-to-text/convert).

The SDK speech synthesis descriptor in `speech-synthesis.json` maps the
workspace credential and caller-supplied voice ID to the ElevenLabs
[Create speech endpoint](https://elevenlabs.io/docs/api-reference/text-to-speech/convert).
It requests MP3 from the Multilingual v2 model and caps each request at
2,500 characters. Arrumo host dispatch is pending.
