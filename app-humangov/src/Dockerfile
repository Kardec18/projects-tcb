# Imagem base
FROM python:3.8-slim-buster

# Working Directory
WORKDIR /app

# Copiar requirements.txt
COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

# Iniciar "Gunicorn"
CMD ["gunicorn", "--workers", "1", "--bind", "0.0.0.0:8000", "humangov:app"]
