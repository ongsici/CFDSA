FROM python:3.10-slim

ENV PORT=3000
ENV INSTANCE_NAME=""
ENV INSTANCE_HASH=""

COPY requirements.txt /app/requirements.txt
WORKDIR /app

RUN pip install -r requirements.txt

COPY ./public public
COPY ./templates templates
COPY main.py .
COPY utils.py .
COPY run.sh .

RUN chmod +x run.sh
ENTRYPOINT ["./run.sh"]

