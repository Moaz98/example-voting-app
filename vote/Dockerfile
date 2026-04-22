# Base Image
FROM python:2.7-alpine

# Set working directory
WORKDIR /app

# Copy application files
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose port
EXPOSE 80

# Run the application
CMD ["gunicorn", "app:app", "-b", "0.0.0.0:80"]
