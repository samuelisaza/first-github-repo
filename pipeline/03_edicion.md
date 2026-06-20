# Edición de Video — @cristobaldiazp

> Proceso: Cristóbal sube el script aprobado + el video raw → Claude produce el video editado o la guía de edición detallada.

---

## CÓMO FUNCIONA

### Input de Cristóbal
1. Script aprobado (texto — puede estar en Drive o pegado directamente)
2. Video raw (subir archivo o compartir link de Google Drive)
3. Indicar: ¿hay múltiples takes? ¿cuál prefiere o deja que Claude elija?

### Output de Claude
- Análisis del video raw: mejor take, timecodes de silencios/errores/tomas débiles
- Composición de video editado via HeyGen HyperFrames (cuando está disponible en sesión)
- O: guía de edición corte a corte con timecodes exactos para ejecutar en CapCut

---

## ESPECIFICACIONES DE EDICIÓN POR ELEMENTO

### Corte y ritmo
- Ritmo de corte: **no mecánico** — los cortes siguen el ritmo de la frase, no el reloj
- Silencios: cortar los >0.8s entre frases (mantener micropausa de 0.3–0.5s para respiración)
- Errores: cortar cualquier duda, repetición o "eh" visible
- Tomas débiles: si el take tiene energía baja en la frase central, marcar para re-grabar antes de editar

### Texto en pantalla
- **Tipografía:** Playfair Display para frases centrales / Inter para información secundaria
- **Colores:** texto blanco `#f5f5f5` sobre fondo oscuro, o navy `#1a3a52` como acento en palabras clave
- **Timing:** el texto aparece **con** la voz, no antes ni después (sincronizado al inicio de la frase)
- **Tamaño:** grande — legible sin audio, sin que tape la cara
- **Zona segura:** evitar los últimos 15% superior e inferior del frame (zona de UI de TikTok/Instagram)
- **Animación:** entrada sutil (fade o deslize lento) — nada que distraiga del contenido

### Subtítulos
- Estilo: palabra a palabra o bloque corto (2–4 palabras) — no párrafos completos
- Fuente: Inter, blanco `#f5f5f5`, borde negro fino para legibilidad sobre cualquier fondo
- La frase central del script va en Playfair Display, tamaño mayor, como momento destacado

### Música / audio de fondo
- Volumen: 10–20% sobre el habla — se siente, no se escucha
- Mood por temperatura del script:
  - **Fría (Séneca, costo hundido, aversión):** ambient minimalista, sin melodía dominante
  - **Cálida (fe, válvula, poema):** cuerdas suaves o piano solo
  - **Neutral filosófico:** cinematográfico instrumental suave
- Entrada: fade in en los primeros 2s / Salida: fade out en los últimos 2s
- No usar audios de tendencia si compiten con el tono del script

### Exportación
- Formato: MP4
- Resolución: 1080 x 1920 (vertical 9:16)
- Framerate: 60fps
- Sin marca de agua
- Nombre de archivo: `ScriptXX_[tema]_final.mp4`

---

## PLANTILLA DE ANÁLISIS DE VIDEO RAW

Cuando Cristóbal sube el video raw, Claude completa esto:

```
Script: XX — [Tema]
Duración raw: __:__
Takes disponibles: [n]

TAKE RECOMENDADO: Take [n]
Razón: [energía, ritmo, entrega de la frase central]

TIMECODES DE EDICIÓN (take seleccionado):
- [00:00–00:03] INTERRUPCIÓN: [descripción]
- [00:03–00:40] HISTORIA MÍNIMA: cortar en [00:XX] (silencio largo / error)
- [00:40–01:10] GIRO: [descripción]
- [01:10–01:30] REMATE: [descripción]

CORTES A HACER:
- [00:XX–00:XX] Silencio largo — cortar
- [00:XX–00:XX] Duda / repetición — cortar
- [00:XX] J-cut recomendado (audio antes del corte visual)

TEXTO EN PANTALLA:
- [00:XX] "[frase]" — Playfair Display, blanco, centro
- [00:XX] "[palabra clave]" — Inter, navy blue, esquina inferior izquierda

MÚSICA RECOMENDADA:
- Mood: [describir]
- Track sugerido: [nombre o tipo de búsqueda en biblioteca libre]

PROBLEMAS DETECTADOS:
- [Si hay algo que requiere re-grabar o ajuste]
```

---

## CAPCUT — REFERENCIA RÁPIDA DE HERRAMIENTAS

*(Para cuando Cristóbal ejecuta la edición manualmente)*

| Necesidad | Herramienta en CapCut |
|---|---|
| Cortar clip | Tijera / Split en el timecode |
| Agregar texto | Texto → elegir fuente Inter o Playfair |
| Subtítulos automáticos | Subtítulos → Auto-generados → ajustar timing |
| Música de fondo | Audio → Biblioteca o importar |
| Color grading | Filtro → Cinematográfico o ajuste manual (brillo -10, contraste +15, saturación -5 para look frío) |
| Exportar | 1080p, 60fps, sin marca de agua (requiere cuenta) |
