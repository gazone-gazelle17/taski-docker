FROM python:3.9
WORKDIR /app
RUN pip install gunicorn==20.1.0
COPY requirements.txt .
COPY . .
RUN pip install -r /app/requirements.txt --no-cache-dir
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]
