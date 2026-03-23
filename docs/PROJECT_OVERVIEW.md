# Project Overview

## Project Name

Hospitality Concept Visualizer

## Purpose

The project is a web application for hospitality concept visualization using multimodal Generative AI. A user enters a hospitality-related prompt, and the system produces:

- a descriptive text concept
- a corresponding concept image

## Main Features

- Prompt-based concept generation
- Text generation using Google Gemini
- Image generation using Hugging Face Stable Diffusion
- Streamlit-based web interface
- Input validation and API error handling
- Modular Python project structure

## Tech Used

- Python
- Streamlit
- Google Gemini API using `google-genai`
- Hugging Face Inference API
- `requests`

## Updated Project Structure

```text
team_handoff_demo/
|-- app/
|   |-- __init__.py
|   `-- main.py
|-- services/
|   |-- __init__.py
|   |-- gemini_service.py
|   `-- image_service.py
|-- database/
|   |-- __init__.py
|   `-- db.py
|-- config/
|   |-- __init__.py
|   `-- config.py
|-- utils/
|   |-- __init__.py
|   `-- utils.py
|-- docs/
|   |-- HLD_REPORT_NOTES.md
|   `-- PROJECT_OVERVIEW.md
|-- .env.example
|-- .gitignore
|-- README.md
`-- requirements.txt
```

## Functional Flow

1. User enters a hospitality prompt in the Streamlit UI.
2. Input is validated in `utils/utils.py`.
3. Prompt is sent to `services/gemini_service.py`.
4. Prompt is sent to `services/image_service.py`.
5. Results are rendered in `app/main.py`.

## Notes

- The `database/` package is included for the next enhancement phase.
- The current version keeps the generation workflow unchanged.
