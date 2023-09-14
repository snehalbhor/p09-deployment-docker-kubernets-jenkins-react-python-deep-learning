# Use an official Python runtime as the base image
FROM python:3.6

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt file to the container
COPY requirements.txt .

# Install Python dependencies
RUN apt-get update && apt-get install libgl1 -y

RUN pip install  -r requirements.txt

# Copy the rest of your application's source code to the container
COPY . .

# Expose the port that your Python app runs on (e.g., 5000)
EXPOSE 5000

# Start your Python app (replace with your actual startup command)
CMD ["python3", "app.py"]
