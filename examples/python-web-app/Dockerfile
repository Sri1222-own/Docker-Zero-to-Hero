FROM ubuntu:20.04

WORKDIR /app

COPY requirements.txt /app/
COPY devops /app/

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install --no-cache-dir --break-system-packages -r requirements.txt

ENV PIP_BREAK_SYSTEM_PACKAGES=1

CMD ["python3", "devops/manage.py", "runserver", "0.0.0.0:8000"]



