# Pull the minimal Ubuntu image
FROM ubuntu:latest

# Install Nginx
RUN export DEBIAN_FRONTEND=noninteractive
RUN apt update
RUN apt install -y python3  python3-pip python3-flask python3-requests vim btop

RUN mkdir -p /blue/templates
COPY . /blue/
WORKDIR /blue


# Run the basic blue server
ENTRYPOINT ["python3", "blue.py"]

CMD ["python3", "blue.py", "runserver" ,"0.0.0.0:5000"]