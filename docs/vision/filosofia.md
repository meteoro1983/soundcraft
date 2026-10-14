# Filosofía — DAW de Matías (fork de SoundCraft)

> Nombre provisorio. Rama de trabajo: `matias`. Upstream: storytold/soundcraft (remoto `upstream`).

## Qué es
Un DAW **de audio** (el MIDI profundo lo cubre el DAW inteligente del hermano de Matías).
Base: SoundCraft (modelo Pro Tools, Rust, clean-room). Encima: la soltura de Sonar y la robustez de Samplitude.

## Pilares
1. **Intuitivo como Sonar/Cakewalk** — sobre todo la **regleta** (timeline). *Pendiente: que Matías describa qué le gusta exactamente.*
2. **Sólido como Samplitude** — bounce confiable y verificable, backups versionados, guardado atómico,
   diario de comandos para recuperar la sesión tras un cierre, plugins de terceros aislados en otro proceso.
3. **Plugins CLAP propios "de batalla"** — integración nativa de primera clase (tira de canal fija tipo ProChannel).
4. **Asistente de mezcla con IA** — analiza (LUFS, espectro, enmascaramiento), propone, aplica como comandos deshacibles. Nunca a ciegas.
5. **Skins / GUI a su manera** — sistema de temas (archivo + imágenes) sin recompilar.

## Fuera de foco
Score, video, MIDI pesado (posible puente/sync con el DAW del hermano más adelante).

## Reglas heredadas que respetamos
- Clean-room: observar Sonar/Samplitude/Pro Tools sí; copiar código, assets, presets o decompilados, nunca.
  Ghidra solo para entender formatos/comportamiento → spec en palabras propias → implementación desde cero.
- "Never crash" de upstream (sin unwrap/panic, errores como Result). Ver `AGENTS.md`.

## Bitácora
- 2026-10-14 — Fork local creado desde upstream v0.7.0 (682 commits). Instalada build oficial portable para familiarizarse.
