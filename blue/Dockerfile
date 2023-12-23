# Pull the minimal Ubuntu image
FROM ubuntu:latest

# Install Nginx
RUN apt update
RUN apt install -y python3  python3-pip vim btop

RUN mkdir -p /blue/templates
WORKDIR /blue
COPY blue.py /blue/
COPY templates/index.html /blue/templates
COPY ./requirements.txt /blue/requirements.txt
RUN pip install --no-cache-dir --upgrade -r /blue/requirements.txt

# Run the basic blue server
ENTRYPOINT ["python3", "blue.py"]

CMD ["python3", "blue.py", "runserver" ,"0.0.0.0:5000"]