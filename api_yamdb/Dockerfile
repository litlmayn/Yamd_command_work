FROM python:3.7-slim
RUN apt update && apt install -y gcc cmake libpq-dev python-dev

WORKDIR /app

COPY . .

RUN pip3 install -r requirements.txt --no-cache-dir

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000"]
