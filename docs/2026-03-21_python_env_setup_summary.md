# ZLab — Python Environment Setup
**Fecha:** 2026-03-21
**Subfase:** 0.8 — Entorno Python aislado
**Repo objetivo:** `~/Workspace/ZLab/repos/zlab-core`

---

## Estado inicial encontrado

| Item | Estado |
|---|---|
| `zlab-core/` | ✅ existía con estructura completa |
| `pyproject.toml` | ✅ existía (se actualizó) |
| `README.md` | ✅ existía |
| `.venv` | ✅ existía — Python 3.12.13 funcional |
| jupyter/numpy/pandas/matplotlib | ❌ no instalados — se instalaron ahora |

## Python elegido

**Python 3.12.13** — `/opt/homebrew/bin/python3.12`

Razón: único Python moderno no-sistema disponible, instalado vía Homebrew en subfase 0.6.
Python del sistema (`/usr/bin/python3` 3.9.6) no se tocó.

## uv utilizado

Sí — `uv 0.10.12` para instalación de paquetes dentro del `.venv`.
El `.venv` ya existía y fue creado previamente con `uv venv`.

## .venv

- Path: `~/Workspace/ZLab/repos/zlab-core/.venv`
- Creado previamente — no se recreó
- Python: 3.12.13
- Ejecutable: `.venv/bin/python`

## Dependencias instaladas (105 paquetes)

| Paquete | Versión |
|---|---|
| numpy | 2.4.3 |
| pandas | 3.0.1 |
| matplotlib | 3.10.8 |
| jupyter | 1.1.1 |
| ipykernel | 7.2.0 |
| jupyterlab | 4.5.6 |
| pytest | 9.0.2 |
| ruff | 0.15.7 |

## Kernel Jupyter registrado

- Nombre interno: `zlab-core`
- Display name: `ZLab Core (Python 3.12)`
- Path: `~/Library/Jupyter/kernels/zlab-core`

## Archivos creados / modificados

- `pyproject.toml` — actualizado con dependencias base
- Kernel Jupyter registrado en `~/Library/Jupyter/kernels/zlab-core`

## Pruebas ejecutadas

| Prueba | Resultado |
|---|---|
| `python --version` dentro del `.venv` | ✅ Python 3.12.13 |
| `import numpy` | ✅ 2.4.3 |
| `import pandas` | ✅ 3.0.1 |
| `import matplotlib` | ✅ 3.10.8 |
| `jupyter --version` | ✅ operativo |
| kernel `zlab-core` visible | ✅ |

## Commits realizados

```
260b815  Add data science deps to pyproject.toml (numpy, pandas, matplotlib, jupyter)
```
Push a `github.com/davidlagarejo/zlab-core` ✅

## Siguiente paso recomendado

**Subfase 0.9 — Verificación final y checklist de preparación ZLab:**
- Verificar extensiones VS Code (Python, Pylance, Ruff)
- Crear `src/zlab/` como paquete Python inicial
- Confirmar que `.venv` no entra en Git (`.gitignore` lo excluye ✅)
- Estrategia de backup: código → GitHub ✅ | data → Seafile en externo ✅
