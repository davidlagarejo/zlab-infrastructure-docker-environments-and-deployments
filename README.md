# ZLab Infrastructure

Setup, bootstrap, configuración no sensible, templates e instrucciones del entorno ZLab.

## Contenido

| Carpeta | Propósito |
|---|---|
| `bootstrap/` | Scripts de instalación y configuración inicial del entorno |
| `scripts/` | Utilidades operativas del lab |
| `configs/` | Configuraciones de herramientas (no sensibles) |
| `docs/` | Documentación técnica del entorno |
| `templates/` | Templates reutilizables (.gitignore, pyproject.toml, etc.) |

## Política de contenido

- ✅ Scripts de setup y automatización
- ✅ Configuraciones no sensibles
- ✅ Documentación de infraestructura
- ❌ Secretos, tokens, API keys
- ❌ Datasets, modelos, outputs pesados
- ❌ Variables de entorno reales (`.env`)

## Entorno

- Python de trabajo: `python3.12` (via Homebrew)
- Gestor de entornos: `uv`
- Rama principal: `main`
