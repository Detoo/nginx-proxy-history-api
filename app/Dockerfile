FROM python:2.7

WORKDIR /opt/nginx-proxy-history-api

COPY requirements.txt ./
RUN pip install -r requirements.txt

ENTRYPOINT ["python", "app.py"]
