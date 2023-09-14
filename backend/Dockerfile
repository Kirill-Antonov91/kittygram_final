FROM python:3.9

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

ENTRYPOINT [ "sh", "command_to_gunicorn.sh" ]

CMD ["command_to_gunicorn.sh"]