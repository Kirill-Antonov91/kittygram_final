FROM python:3.9

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

RUN chmod 700 command_to_gunicorn.sh

ENTRYPOINT ["./command_to_gunicorn.sh"]

CMD ["fake cmd for pytest"]