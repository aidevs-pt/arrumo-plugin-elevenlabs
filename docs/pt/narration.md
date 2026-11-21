# Narre vídeos com o ElevenLabs

[English](../en/narration.md) · [Español](../es/narration.md)

Quando um vídeo começa do zero, o Arrumo constrói-o com cenas animadas e o agente escreve uma frase de narração para cada uma. Se o ElevenLabs for o primeiro na ordem de fornecedores de texto para voz e tiver uma chave de API, o Arrumo dá voz a cada frase ao criar a pré-visualização, alonga as cenas que precisam de mais tempo e reutiliza o mesmo áudio no vídeo final. As legendas seguem a narração.

Para escolher a voz, copie um ID de voz da sua biblioteca de vozes do ElevenLabs e cole-o em **Voice ID** nas definições do plugin para o espaço de trabalho. Se estiver vazio, o Arrumo usa George. Cada tentativa de pré-visualização volta a sintetizar a narração, o que gasta créditos do ElevenLabs. Se a síntese falhar, a pré-visualização é criada sem narração e o motivo aparece no resumo.
