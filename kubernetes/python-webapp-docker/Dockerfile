FROM python:3.8-slim-buster

RUN groupadd --gid 1000 app && \
    useradd --create-home --gid 1000 --uid 1000 app

RUN mkdir -p /home/app/src

WORKDIR /home/app/src

COPY ./ /home/app/src

RUN pip3 install Flask==2.0.2 gunicorn==20.0.4

USER app

ENTRYPOINT ["gunicorn"]

CMD ["app:app"]
