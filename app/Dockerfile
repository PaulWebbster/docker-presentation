FROM python:3.9

LABEL maintainer="Pawel Weber <pawel.weber@thaumatec.com>"

LABEL name="Docker essentials workshop docker"

RUN mkdir /app

WORKDIR /app

# Install python requirements.txt
COPY requirements.txt /app/requirements.txt

RUN pip install -r /app/requirements.txt

# Add application to container
COPY application.py /app/application.py

# Export flask app
RUN export FLASK_APP=/app/application.py

# Label ports to be used with container
EXPOSE 5000/tcp

# Set entrypoint to our container
ENTRYPOINT ["flask", "run"]

