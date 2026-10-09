# edgar-vela.ch

Professional engineering portfolio for **Edgar Vela** (Hardware & Embedded Systems Engineer), built with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and hosted on GitHub Pages.

## Local Development

1. Create and activate a Python virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the development server:
   ```bash
   mkdocs serve
   ```
   Open `http://127.0.0.1:8000` in your browser.

## Deployment

Pushes to the `main` branch automatically build and deploy the site to the `gh-pages` branch via GitHub Actions (`.github/workflows/deploy.yml`).
