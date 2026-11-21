# Narra vídeos con ElevenLabs

[English](../en/narration.md) · [Português](../pt/narration.md)

Cuando un vídeo empieza desde cero, Arrumo lo construye con escenas animadas y el agente escribe una frase de narración para cada una. Si ElevenLabs es el primero en el orden de proveedores de texto a voz y tiene una clave de API, Arrumo pone voz a cada frase al crear la vista previa, alarga las escenas que necesitan más tiempo y reutiliza el mismo audio en el vídeo final. Los subtítulos siguen la narración.

Para elegir la voz, copia un ID de voz de tu biblioteca de voces de ElevenLabs y pégalo en **Voice ID** en los ajustes del plugin para el espacio de trabajo. Si está vacío, Arrumo usa George. Cada intento de vista previa vuelve a sintetizar la narración, lo que consume créditos de ElevenLabs. Si la síntesis falla, la vista previa se crea sin narración y el motivo aparece en su resumen.
