# resume_analyser

Resume Matcher compares an uploaded PDF or DOCX resume with the sample job description using the Groq API.

## Run locally

1. Install [uv](https://docs.astral.sh/uv/).
2. Set `GROQ_API_KEY` in a local `.env` file (see `.env.example`).
3. From this directory, run:

   ```powershell
   uv sync
   uv run python app.py
   ```

4. Open `http://localhost:5000`.

## Deploy on Render

Create a Render Web Service from this repository and set `GROQ_API_KEY` as a secret environment variable. The included `render.yaml` configures the build and Gunicorn start commands.

Uploaded resumes are processed by the service and are not intended to be committed to the repository.
