# Proyecto MkDocs: Redes informaticas

## Requisitos
- Python instalado
- pip instalado
- Cuenta de GitHub

## Instalacion
Abre una terminal en esta carpeta y ejecuta:

```bash
python -m pip install -r requirements.txt
```

## Previsualizar la web

```bash
mkdocs serve
```

Abre la direccion que aparece en la terminal (normalmente http://127.0.0.1:8000/).

## Generar la web

```bash
mkdocs build
```

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub con el nombre `PI_P3_MkDocs_Redes`.
2. Inicializa Git en esta carpeta y sube los archivos:

```bash
git init
git add .
git commit -m "Primer commit: proyecto MkDocs"
git branch -M main
git remote add origin https://github.com/USUARIO/PI_P3_MkDocs_Redes.git
git push -u origin main
```

3. Publica la web ejecutando:

```bash
mkdocs gh-deploy
```

4. En GitHub, entra en **Settings > Pages** y comprueba que la fuente de despliegue sea la rama `gh-pages`.
5. Sustituye `USUARIO` en `mkdocs.yml` y en los comandos por tu nombre de usuario real de GitHub.

La URL final tendra este formato:

`https://USUARIO.github.io/PI_P3_MkDocs_Redes/`

## Estructura

- `mkdocs.yml`: configuracion y navegacion.
- `docs/`: paginas Markdown.
- `docs/img/`: imagenes utilizadas.
- `docs/css/`: personalizacion visual.
