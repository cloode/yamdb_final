FROM python:3.8-slim

WORKDIR /app

COPY . .

RUN pip3 install --upgrade pip; \
    pip3 install -r requirements.txt --no-cache-dir 

COPY api_yamdb/ .

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]