FROM python:3.8-slim

WORKDIR /rates

COPY requirements.txt .
RUN pip3 install -Ur requirements.txt

COPY . .

ENTRYPOINT ["gunicorn"]

CMD ["-b", ":3000", "wsgi"]
