# agentic-marketplace

Marketplace de **producción** de la organización. Lo lee toda la organización.

No contiene artefactos: sólo el índice de dónde están. Para cada unidad publicada lista su última
versión **final** (sin sufijo de prelanzamiento). El índice no se edita: lo regenera
`rebuild-index.yml` cada vez que un dominio publica y una vez al día como red de seguridad.

| Ruta | Quién la lee |
|---|---|
| `.claude-plugin/marketplace.json` | Claude Code |
| `.github/plugin/marketplace.json` | GitHub Copilot CLI |

Las dos rutas se generan desde la misma lista de releases para que no puedan divergir.

El canal lo declara la variable de repositorio `INDEX_CHANNEL` (`production`), no el nombre del repo.
Los dominios se descubren por el topic de repositorio declarado en `AGENTIC_TOPIC` (`agentic-unit`).

## Estado

Esqueleto del hito 0. El workflow queda como marcador hasta su spec en `agentic-standard`.
