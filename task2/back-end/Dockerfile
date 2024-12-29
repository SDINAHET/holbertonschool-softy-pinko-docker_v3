# Use the latest Ubuntu image
FROM ubuntu:latest

# Update APT and upgrade installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Handle externally managed Python environment issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install flask

# Set /app as the working directory
WORKDIR /app

# Copy the api.py file into the Docker image
COPY ./api.py /app/api.py

# Expose port 5252 for the Flask app
EXPOSE 5252

# Set the default command to run the Flask app
CMD ["python3", "api.py"]
