FROM python:3.10-slim-buster

# Set the working directory inside the container
WORKDIR /backend-flask

# Copy the requirements.txt file from the current directory, into the working dir inside the container
COPY requirements.txt requirements.txt

# Install the libraries defined in the requirements.txt file
RUN pip3 install -r requirements.txt

# Copy all the files in the current directory (outside container), into the working directory
COPY . .

# Set the env variables
ENV FLASK_ENV=development
ENV FRONTEND_URL="*"
ENV BACKEND_URL="*"

EXPOSE ${PORT}
# python3 -m flask run --host 0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]