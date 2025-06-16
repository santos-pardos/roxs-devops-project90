# Usa una imagen oficial de Python bien ligera
FROM python:3.12-slim

# Ajustes básicos
ENV PYTHONUNBUFFERED=1 \
    PIP_NO_CACHE_DIR=1 \
    PORT=80

WORKDIR /app

# Instalar dependencias primero (capa caché)
COPY vote/requirements.txt .
RUN pip install -r requirements.txt

# Copiamos el resto del código
COPY vote/ .

# Expone el puerto HTTP
EXPOSE 80

# Lanzamos la app Flask
CMD ["python", "app.py"]
