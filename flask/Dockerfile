FROM ubuntu:16.04

LABEL Maintainer="Moïse Kamgoué <moise@kamgoue.me>" \
      Description="API REST using Flask"

RUN apt-get update -y && \
    apt-get install -y python-pip python-dev

# We copy just the requirements.txt first to leverage Docker cache
COPY ./src/requirements.txt /app/requirements.txt
RUN pip install -r requirements.txt
WORKDIR /app
COPY ./src/ /app

ENTRYPOINT [ "python" ]

CMD [ "app.py" ]