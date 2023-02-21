FROM python:3.10-slim-buster

# Constainer
# make a new folder inside the container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# this contains the libraries we want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container -> Inside Conatiner
# Install python libraries used for the app
RUN pip3 install -r requirements.txt

# . means everything in the current directory
# first . is everything in /backend-flask (Outside container)
# second . is everything in backend-flask (Inside container)
COPY . .

# Set envirenment variables (Env Vars)
#Insdie container and will remain set when the conatineris run
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# python -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]