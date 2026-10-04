# Invoice Automation Lab - Runnable Code

Companion code for the guide
**[The Invoice Automation Lab](https://vinitshetty.github.io/mistral-devguides/guide.html?id=invoice-automation-lab)**:
durable invoice processing with Mistral Workflows - OCR extraction, structured
JSON, human approval signals, and crash-resume.

## Run it

```bash
uv sync
cp .env.example .env   # set MISTRAL_API_KEY and DEPLOYMENT_NAME
```

Terminal 1 - start the worker:

```bash
uv run --frozen python workflows/workflow/worker.py
```

Terminal 2 - process an invoice:

```bash
uv run --frozen python workflows/workflow/run.py invoices/batch1-1472.jpg
```

Approvals, crash-resume batches, and the full walkthrough are in the guide.
