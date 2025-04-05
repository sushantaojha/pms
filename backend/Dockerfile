#pull base image
FROM python:3.9.7-slim

#creating app folder where the code will reside in container
WORKDIR /app

#copy the dependency related file from source host to container
COPY requirements.txt .

RUN pip install --upgrade pip

#install pip dependencies
RUN pip install --no-cache-dir -r requirements.txt

#copy rest of the application code
COPY . .

#expose port
EXPOSE 8001

#run python
CMD ["python", "manage.py", "runserver", "0.0.0.0:8001"]
