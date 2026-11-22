# Ajedrez desde cero · arquitectura (v0.1.0, 22-nov-2026)

- Stack: TypeScript + Bun (igual que Naipera), sin React (vanilla TS). Web estática en `public/` (index.html + app.js + bot.js en Web Worker). Docker: nginx:alpine sirviendo `public/`, puerto 8080.
- Motor de reglas propio (`src/engine/chess.ts`) validado con perft estándar (5 posiciones de chessprogramming.org).
- Máquina (`src/engine/bot.ts`): alfa-beta + quiescencia; niveles Principiante / Fácil / Normal; pistas; aviso de pérdida de material (solo material, sin amenazas de mate).
- Curso (`src/curso/lecciones.ts`): 33 lecciones en 8 módulos. Tipos de paso: texto, pregunta, casilla, marcar, estrellas, jugada, partida. Tests validan cada posición, solución y respuesta.
- Consolidación: lecciones en orden (bloqueo), 1-3 estrellas según fallos, 2 repasos por lección desde la 3.ª, sesión de Repaso de 8 ejercicios ponderada por fallos y tiempo sin ver; glosario que se abre al completar lecciones.
- Ayudas en Jugar: Aprendiz / Jugador / Sin ayudas (sistema de Naipera).
- Progreso solo en localStorage (sin cuentas).
- Pendiente: publicar en URL (p. ej. Cloudflare Worker de static assets en ajedrez.naipera.com), probar con usuarios reales.
