# Pull the minimal Ubuntu image
FROM ubuntu:latest

# Install Nginx
RUN apt update
RUN apt install -y python3  python3-pip vim btop

RUN mkdir -p /blue/templates
COPY . /blue/
WORKDIR /blue
RUN /usr/bin/pip3 install -r /blue/requirements.txt


# Run the basic blue server
ENTRYPOINT ["python3", "blue.py"]

CMD ["python3", "blue.py", "runserver" ,"0.0.0.0:5000"]