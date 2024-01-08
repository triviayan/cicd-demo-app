FROM python:3.8-slim-buster

WORKDIR /app

# Install dependencies first to leverage Docker layer caching
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

# Copy the rest of the application code
COPY . .

# Specify the command to run your application
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]
