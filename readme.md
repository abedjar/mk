# MkDocs Material – Local Development with Docker

This project uses **MkDocs Material** running entirely in Docker.  
No Python, no virtualenv, no local dependency mess.

---

## Requirements

- Docker installed and running
- Port **8000** available on your machine

That’s it.

---

## Project Structure

Expected layout:
```bash
.
├── mkdocs.yml
├── docs/
│   └── index.md
└── README.md
```
* `mkdocs.yml` – MkDocs configuration
* `docs/` – Markdown content
* Everything is mounted into the container at /docs


---

## Run MkDocs Locally

From the root of your documentation project:

```bash
docker run --rm -it \
  --entrypoint sh \
  -p 8000:8000 \
  -v "$PWD":/docs \
  squidfunk/mkdocs-material
```

This will open and interactive shell in the container.

Once inside the container shell, start the development server:

```bash
mkdocs serve --livereload -a 0.0.0.0:8000
```

Shell's output after the above command should look like:
```
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.51 seconds
INFO    -  [21:59:14] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [21:59:14] Serving on http://0.0.0.0:8000/
```
---

The `--livereload` flag is crucial to enable direct refresh after saving.

## Access the Site

Open your browser:
[http://localhost:8000](http://localhost:8000)

Changes to files are picked up automatically thanks to live reload.

---


## Notes

- The container is ephemeral (--rm). Nothing persists except your local files.
- All edits happen on your host machine.
- The server binds to 0.0.0.0 so Docker port mapping works correctly.
- If port 8000 is already in use, change the -p value.

Example:
```
-p 9000:8000
```

Then open:

```
http://localhost:9000
```