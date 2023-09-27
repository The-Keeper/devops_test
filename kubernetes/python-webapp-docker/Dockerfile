FROM python:3.8-slim-buster

WORKDIR /python-docker

RUN pip3 install Flask==2.0.2

COPY . .

CMD [ "python3", "app.py"]
