FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app/devops

    
RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv && \
    python3 -m pip install --upgrade pip && \
    pip install -r requirements.txt

ENTRYPOINT ["python3"]
CMD ["devops/manage.py", "runserver", "0.0.0.0:8000"]




