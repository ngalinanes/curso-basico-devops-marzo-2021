FROM python:3.7

ENV PYTHONUNBUFFERED 1
ENV SECRET_KEY somesecret

WORKDIR /backend

COPY . .

RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y python3-dev graphviz libgraphviz-dev pkg-config && \
    pip install --upgrade pip && \
    pip install -r requirements.txt

EXPOSE 8000

COPY . /backend/