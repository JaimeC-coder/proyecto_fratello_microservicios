# Imagen base de Python
FROM python:3.12.5
WORKDIR /app_django
COPY requirements.txt .
RUN apt-get update
RUN apt-get install -y gcc
RUN apt-get install -y python3-dev
RUN apt-get install -y libpq-dev
RUN apt-get install -y python3-psycopg2
RUN apt-get install -y python3-pip
RUN apt-get install -y python3-venv
RUN apt-get install -y python3-wheel
RUN apt-get install -y python3-setuptools
RUN apt-get install -y python3-cffi
RUN apt-get install -y python3-cryptography 
RUN apt-get install -y python3-openssl
RUN apt-get install -y python3-pycparser
RUN apt-get install -y python3-requests
RUN apt-get install -y python3-urllib3
RUN apt-get install -y python -v
RUN python -m pip install --upgrade pip

RUN pip install -r requirements.txt
COPY . .
EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
