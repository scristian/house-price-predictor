# Use the official Python 3.9 slim image as the base
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy requirements first (for better caching)
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose Streamlit's default port
EXPOSE 8501

# Set the command to run the Streamlit app
CMD ["streamlit", "run", "app.py", "--server.address=0.0.0.0"]
