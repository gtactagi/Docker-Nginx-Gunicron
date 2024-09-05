# Usa una imagen base de Python
FROM python:3.9-slim

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos de requerimientos y los instala
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copia todo el código de la aplicación
COPY . /app/

# Expone el puerto 8000 (el puerto que usará Gunicorn)
EXPOSE 8000

# Comando para correr la aplicación con Gunicorn
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "mi_django_proyecto.wsgi:application"]
