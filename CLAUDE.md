## graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships.

Rules:
- When graphify-out/graph.json exists, run `graphify query "<question>"` before your first grep, search or source-file read for a codebase question, and put this rule in every subagent prompt that explores code. Read raw files only for lines the graph or an earlier read already located. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying code, run `graphify update .` to keep the graph current (AST-only, no API cost).
- A committed graphify-out/graph.json is rewritten whole on every build, so a large diff to it in a pull request is expected. Do not flag it as churn or suggest skipping the graph rebuild or its hooks.

## Sobre el usuario y cómo trabajar con él

- Responde siempre en español.
- El usuario está aprendiendo a usar Claude Code y Git/GitHub: explica los conceptos con palabras sencillas (qué es una rama, un pull request, un merge…) y sin dar por hecho conocimientos previos.
- Usa Claude Code desde un iPhone, en sesiones en la nube. Cuando haga falta una acción suya en GitHub (por ejemplo unir un pull request), dale el enlace directo y los botones exactos que debe pulsar.
- Las sesiones son temporales: todo lo que deba conservarse hay que subirlo a GitHub.
- Recomendación acordada: trabajar con un solo repositorio por sesión.

## Contexto del proyecto

- ClearVision v6 es un tema para Discord (BetterDiscord) escrito en SCSS. El punto de entrada es `main.scss`; los ajustes del usuario son variables CSS en `src/defaultSettings.scss`, que llegan a los componentes a través del mapa `$cv` y la función `cv()`.
- graphify sirve para mapear el código, no para recordar conversaciones. Como graphify no reconoce archivos `.scss`, `graphify update .` no los vuelve a leer: tras cambios grandes en SCSS hay que regenerar el grafo incluyendo el SCSS de forma manual en la extracción semántica.
