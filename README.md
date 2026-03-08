# hello-world-demo

A minimal FastAPI web server that renders a simple **Hello World** web page.

## Setup

```bash
python3 -m pip install -r requirements.txt
```

## Run

```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

Then open: <http://localhost:8000>


## GitHub Actions Review Workflow

This repository includes a workflow at `.github/workflows/review-server.yml` that:

1. Installs dependencies.
2. Starts the FastAPI server in CI.
3. Fetches `/` into `review.html`.
4. Uploads `review.html` and `server.log` as a workflow artifact named `web-server-review`.

To run it manually:

1. Open the **Actions** tab in GitHub.
2. Select **Review Web Server**.
3. Click **Run workflow**.
4. Download the `web-server-review` artifact to review the rendered page output.
