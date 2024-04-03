# Use an official Python runtime as a parent image
FROM python

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app if there is no volume mount 
#COPY ./llama_cpu_webapp.py /app/llama_cpu_webapp.py
#COPY llama-2-7b-chat.Q2_K.gguf /app/llama-2-7b-chat.Q2_K.gguf

# Install any needed packages specified in requirements.txt
RUN pip install llama-cpp-python
RUN pip install gradio

# Expose port 7860 to the world outside this container if not exposed in service.yml, deployment.yml and nginx-ingress.yml
#EXPOSE 7860

# Run app.py when the container launches
CMD ["python", "llama_webapp.py"]