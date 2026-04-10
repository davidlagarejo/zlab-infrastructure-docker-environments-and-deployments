# ZLab — Git Setup Summary
**Fecha:** 2026-03-21
**Subfase:** 0.7 — Base local de versionado

---

## Estado inicial encontrado

| Item | Estado |
|---|---|
| `~/Workspace/ZLab` | ✅ existía |
| `~/Workspace/ZLab/repos` | ✅ existía, vacío |
| Git | ✅ 2.50.1 (Apple Git) |
| gh | ✅ 2.88.1 |
| `git user.name` | ❌ no estaba configurado |
| `git user.email` | ❌ no estaba configurado |
| `init.defaultBranch` | ❌ no estaba configurado |

## Configuración Git global aplicada

```
user.name  = David Lagarejo
user.email = [configured locally]
init.defaultBranch = main
```

## Repos creados

| Repo | Path | Rama |
|---|---|---|
| zlab-infra | `~/Workspace/ZLab/repos/zlab-infra` | `main` |
| zlab-core | `~/Workspace/ZLab/repos/zlab-core` | `main` |

## Archivos creados por repo

### zlab-infra
- `.gitignore`
- `README.md`
- `bootstrap/.gitkeep`
- `scripts/.gitkeep`
- `configs/.gitkeep`
- `docs/.gitkeep` + `docs/2026-03-21_git_setup_summary.md`
- `templates/.gitkeep`

### zlab-core
- `.gitignore`
- `README.md`
- `src/.gitkeep`
- `tests/.gitkeep`
- `docs/.gitkeep`
- `scripts/.gitkeep`
- `prompts/.gitkeep`
- `configs/.gitkeep`
- `examples/.gitkeep`

## Commits realizados

- `zlab-infra`: "Initialize zlab-infra base structure"
- `zlab-core`: "Initialize zlab-core base structure"

## ⚠️ Sin push remoto

No se ha configurado ningún remote. No se ha hecho push a GitHub.
Ambos repos son **solo locales** en este momento.

## Siguiente paso recomendado

**Subfase 0.8** — Configurar entorno Python aislado con `uv`:
```bash
cd ~/Workspace/ZLab/repos/zlab-core
uv venv --python 3.12
```
Luego: configurar `pyproject.toml`, instalar dependencias base, y conectar VS Code al entorno correcto.

Cuando sea necesario subir a GitHub:
```bash
gh auth login
gh repo create zlab-infra --private
```
