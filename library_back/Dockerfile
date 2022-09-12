# Build linux image and python
FROM ubuntu:20.04
RUN apt-get update && apt-get install -y python3.9 python3.9-dev
RUN apt install build-essential -y
RUN apt install python3-pip -y
RUN apt install libpq-dev -y

# Set working dir to /backend
WORKDIR /backend

# Copying requirements
COPY requirements.txt requirements.txt

# Install requirements
RUN pip install -r requirements.txt

# Exposing port 8000
EXPOSE 8000

# Copying all contents in dir to workdir
COPY . .

# Executing backend application
#RUN python3 manage.py makemigrations
#RUN python3 manage.py migrate
#RUN python3 manage.py runserver