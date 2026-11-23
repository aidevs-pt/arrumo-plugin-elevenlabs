<p align="center">
  <img src="icon.svg" width="88" height="88" alt="">
</p>

<h1 align="center">ElevenLabs for Arrumo AI Video Editor</h1>

<p align="center">Narration, music, sound effects, transcription, voice changing and dubbing from ElevenLabs.</p>

<p align="center">
  <a href="LICENSE"><img alt="License: AGPL-3.0" src="https://img.shields.io/badge/license-AGPL--3.0-2337B4"></a>
  <img alt="Bundled with Arrumo" src="https://img.shields.io/badge/bundled%20with-Arrumo-2337B4">
  <a href="https://www.aidevs.pt/tools/arrumo/docs/plugins/elevenlabs/narration"><img alt="Docs in English, Spanish and Portuguese" src="https://img.shields.io/badge/docs-EN%20%C2%B7%20ES%20%C2%B7%20PT-111"></a>
</p>

This plugin ships with [Arrumo AI Video Editor](https://github.com/aidevs-pt/arrumo-video-editor), the free, open-source desktop app where an AI agent writes, designs, voices and cuts your videos and you approve every step. It is turned on in a fresh install; manage it in **Settings › Plugins**.

## Guides

- **Narration, music and sound**: [English](https://www.aidevs.pt/tools/arrumo/docs/plugins/elevenlabs/narration) · [Español](https://www.aidevs.pt/es/tools/arrumo/docs/plugins/elevenlabs/narration) · [Português](https://www.aidevs.pt/pt/tools/arrumo/docs/plugins/elevenlabs/narration)
- **Transcription and subtitles**: [English](https://www.aidevs.pt/tools/arrumo/docs/plugins/elevenlabs/transcription) · [Español](https://www.aidevs.pt/es/tools/arrumo/docs/plugins/elevenlabs/transcription) · [Português](https://www.aidevs.pt/pt/tools/arrumo/docs/plugins/elevenlabs/transcription)

## What it covers

| Capability | Descriptor | ElevenLabs API |
| --- | --- | --- |
| Transcription | `transcription.json` | Speech to text |
| Narration | `speech-synthesis.json` | Text to speech: Multilingual v2 (default), Eleven v4, Eleven v3, Flash v2.5, Flash v2 |
| Music and sound effects | `audio-generation.json` | Music (`music_v2_5`) and sound effects (`eleven_text_to_sound_v3`) |
| Voice changer and voice isolation | `audio-transform.json` | Speech to speech (up to 5 minutes) and audio isolation (4.6 seconds to 1 hour) |
| Dubbing | `dubbing.json` | Dubbing into 29 languages, up to 1 hour |

Music, dubbing and some models need a paid plan. When the plan lacks a feature, Arrumo shows
ElevenLabs' HTTP 402 answer as a plain message. Voice design, voice cloning, text to dialogue and
forced alignment are not covered.

## Remaining credits

`usage.json` reads `GET /v1/user/subscription` (`character_count` of
`character_limit`, resetting at `next_character_count_reset_unix`) with the
[Plugin SDK usage adapter](https://github.com/aidevs-pt/arrumo-plugin-sdk#describe-a-usage-adapter).
Arrumo shows the share left in Settings › Services and keys and warns at 20%
and 10%. Restricted keys need the **User: Read** permission for this; without
it Arrumo shows the usage as unknown (`missing_permissions`) and everything
else keeps working.

## Package a release candidate

From this checkout, use the Arrumo Plugin SDK packager with the adapter files
listed explicitly. Record the SDK commit and the SHA-256 printed by the tool.

```sh
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include usage.json --include speech-synthesis.json --include audio-generation.json --include audio-transform.json --include dubbing.json
```

## Icon and trademarks

`icon.svg` uses the ElevenLabs "11" symbol, unmodified, on a square holding shape, as the
ElevenLabs brand guidelines (https://elevenlabs.io/brand) recommend for app ecosystems. It only
identifies the service this plugin connects to. ElevenLabs and its logo are trademarks of
ElevenLabs. This plugin is not affiliated with or endorsed by ElevenLabs, and the mark is not
covered by this repository's license.

## License

Copyright © 2026 DEVS AI Unipessoal LDA. Licensed under the [GNU Affero General Public License v3.0](LICENSE). Built by [DEVS AI](https://aidevs.pt), who make custom AI solutions for companies.
