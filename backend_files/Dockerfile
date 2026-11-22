
# Use an official Python runtime as a base image
FROM python:3.9-slim

# set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . .

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements

# define the command to start the application using Gunicorn with 4 worker processes
CMD ["gunicorn", "-W", "4", "-b", "0.0.0.0:7860", "app:superkart_api"]
