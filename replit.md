# Киндербург (Kinderburg)

A Flask-based promotional/informational website for an educational center.

## Stack

- **Language**: Python 3.12
- **Framework**: Flask >= 2.3.0
- **Server (prod)**: Gunicorn
- **Frontend**: Jinja2 templates + Bootstrap 5 (CDN)

## Project Layout

- `server.py` — Flask app entry point, serves on `0.0.0.0:5000`
- `requirements.txt` — Python dependencies
- `templates/alogritmika.html` — Main single-page template
- `static/css/main.css` — Custom styles
- `static/` — Images, PDFs, video assets

## Running Locally

```
python3 server.py
```

App runs on port 5000.

## Deployment

Uses Gunicorn via autoscale deployment:

```
gunicorn --bind=0.0.0.0:5000 --reuse-port server:app
```
