# Use an official Python runtime as a parent image
FROM python:3.8

# Set the working directory to /app/back
WORKDIR /app/back

# Copy the contents of the local app/back directory to the container
COPY . /app/back

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port that Flask will run on
EXPOSE 5000

# Define the command to run your application
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]
