# Arrumo ElevenLabs Plugin

The default ElevenLabs adapter for transcription and audio generation.

## Icon and trademarks

`icon.svg` uses the ElevenLabs "11" symbol, unmodified, on a square holding shape, as the
ElevenLabs brand guidelines (https://elevenlabs.io/brand) recommend for app ecosystems. It only
identifies the service this plugin connects to. ElevenLabs and its logo are trademarks of
ElevenLabs. This plugin is not affiliated with or endorsed by ElevenLabs, and the mark is not
covered by this repository's license.

## Transcription and subtitles

[English](docs/en/transcription.md) · [Español](docs/es/transcription.md) · [Português](docs/pt/transcription.md)

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
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include usage.json --include speech-synthesis.json
```
