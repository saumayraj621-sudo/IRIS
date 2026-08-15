# IRIS — Project Structure

## Overview

IRIS is organized into separate sections for the web application, project screenshots, and documentation.

## Structure

```text
IRIS/
├── screenshots/        # Project demonstration images
├── web/                # Flask web application
│   ├── static/         # CSS and image assets
│   ├── templates/      # HTML templates
│   ├── __init__.py
│   ├── app.py          # Main Flask application
│   └── report.py       # Report generation
├── requirements.txt    # Python dependencies
├── .gitignore          # Ignored files and folders
├── LICENSE             # Project license
└── README.md           # Project documentation
```

## Web Application

The `web/` directory contains the main web interface of IRIS. Flask handles the application, while the `templates` and `static` directories contain the frontend resources.

## Screenshots

The `screenshots/` directory contains demonstration images showing the IRIS interface and project workflow.
