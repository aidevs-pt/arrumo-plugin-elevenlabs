# Narrate videos with ElevenLabs

[Español](../es/narration.md) · [Português](../pt/narration.md)

When a video starts from scratch, Arrumo builds it from animated scenes, and the agent writes a line of narration for each one. If ElevenLabs is first in the text-to-speech provider order and has an API key, Arrumo voices each line while making the video preview, lengthens scenes that need more time, and reuses the same audio in the final video. The subtitles follow the narration.

To choose the voice, copy a voice ID from your ElevenLabs voice library and paste it in **Voice ID** in the plugin's workspace settings. When it is empty, Arrumo uses George. Each preview attempt synthesizes the narration again, which uses your ElevenLabs credits. If synthesis fails, the preview is made without narration and the reason is shown in its summary.
