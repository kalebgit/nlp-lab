# lab-nlp

Laboratorio de experimentos de NLP (Hugging Face `transformers`, `datasets`, `peft`, `trl`, `gensim`, etc.).

## Requisitos previos (por máquina, no vienen con el repo)

Estas herramientas se instalan a nivel de sistema operativo y **no** quedan registradas en `pyproject.toml`/`uv.lock`, así que hay que instalarlas manualmente en cada máquina nueva:

- **[uv](https://docs.astral.sh/uv/)** — gestor de paquetes/entornos usado en este proyecto.
- **Python 3.12** (ver `.python-version`). Si no lo tienes, `uv` puede descargarlo solo al correr `uv sync`.
- **GPU / CUDA (opcional):** el proyecto usa `torch`, `transformers`, `accelerate`, `peft` y `trl`. Si vas a entrenar/fine-tunear con GPU, necesitas los drivers NVIDIA y CUDA instalados en el sistema (o el runtime de CUDA para WSL si trabajas en WSL2). `uv sync` instala PyTorch pero no instala drivers de sistema.

## Instalación del proyecto

```bash
git clone <url-del-repo>
cd lab-nlp
uv sync
```

`uv sync` crea el entorno virtual (`.venv`) e instala todas las dependencias fijadas en `uv.lock`.

## Uso

```bash
uv run jupyter notebook
```

o para correr el script principal:

```bash
uv run main.py
```

## Notas

- Los datasets, modelos entrenados y material de referencia (PDFs, etc.) están excluidos del repo vía `.gitignore` por tamaño/derechos. Si el trabajo depende de alguno, hay que copiarlo manualmente a la nueva máquina.
