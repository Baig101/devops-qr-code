# Step 1: Use an official Python runtime as a parent image
FROM python:3.9-slim

# Step 2: Set the working directory in the container
WORKDIR /app

# Step 3: Copy the current directory contents (your app) into the container
COPY . /app

# Step 4: Install any dependencies required for your application
RUN pip install --no-cache-dir -r requirements.txt

# Step 5: Expose the port your application will be running on (default for FastAPI is 8000)
EXPOSE 8000

# Step 6: Define the command to run your application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
