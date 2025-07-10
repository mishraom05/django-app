# Base Image
FROM python:3.9.7-slim AS build

# Copy application related files into app folder
COPY . /app

# Setting app folder as the working-directory 
WORKDIR /app

# Creating the virtual environment
RUN python3 -m venv /opt/venv

# Installing the dependencies 
RUN /opt/venv/bin/pip install --upgrade pip && \
    /opt/venv/bin/pip install -r requirements.txt && \
    chmod +x entrypoint.sh

# Execution of entrypoint.sh script
CMD [ "/app/entrypoint.sh" ]

