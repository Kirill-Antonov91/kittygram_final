FROM python:3.9

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

COPY command_to_gunicorn.sh .

RUN chmod 777 /app/command_to_gunicorn.sh

ENTRYPOINT ["/app/command_to_gunicorn.sh"]

CMD ["gunicorn", "--bind", "0.0.0.0:9000", "kittygram_backend.wsgi"]