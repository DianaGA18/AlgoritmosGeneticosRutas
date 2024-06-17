# Usa una imagen base oficial de Python
FROM python:3.10

ENV PYTHONUNBUFFERED=1

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia el archivo de requisitos
COPY ./requirements.txt ./

# Instala las dependencias
RUN pip install --no-cache-dir -r requirements.txt

# Copia el código de la aplicación al contenedor
COPY ./ ./

# Expone el puerto en el que correrá la aplicación
EXPOSE 8000

# Define el comando para correr la aplicación
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
