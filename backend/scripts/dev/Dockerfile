FROM python:3.7

# This keeps Python from buffering stdin/stdout
ENV PYTHONUNBUFFERED 1

# This prevents Python from writing out .pyc files
ENV PYTHONDONTWRITEBYTECODE 1

RUN mkdir /code
WORKDIR /code

COPY requirements/* /code/requirements/

RUN cat requirements/* > requirements.txt \
    && pip install -r requirements.txt

# COPY scripts/dev/start_dev.sh /
ADD . /code/
