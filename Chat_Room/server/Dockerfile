FROM ubuntu:latest
LABEL authors="aditijain"

ENTRYPOINT ["top", "-b"]

FROM python:3.9

WORKDIR /app

COPY . /app


COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip setuptools
RUN pip install --no-cache-dir --verbose -r requirements.txt

COPY . .

CMD ["python", "start.py"]