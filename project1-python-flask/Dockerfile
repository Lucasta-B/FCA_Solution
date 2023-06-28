FROM python:3

LABEL maintainer="qa.com"
WORKDIR /usr/src/app

COPY ./src/*.py ./
COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

CMD [ "python", "./app.py" ]