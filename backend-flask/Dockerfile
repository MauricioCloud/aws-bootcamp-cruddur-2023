FROM python:3.10-slim-buster

# Inside Container
# Make a new folder inside the container
WORKDIR /backend-flask

# Outside Container -> Inside Container
COPY requirements.txt requirements.txt

# Inside Container
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
COPY . .

# Set environment variables
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD (Command)

# export FRONTEND_URL="*" just for test
# export BACKEND_URL="*" just for test
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567"]

# /api/activities/home just for test
# docker build -t backend-flask ./backend-flask
# FRONTEND_URL="*" BACKEND_URL="*" 
# docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask

