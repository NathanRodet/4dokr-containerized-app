FROM python:3.7

LABEL description = "Deploy a simple flask api"
LABEL maintainer = "Rodet Nathan <rodetnathan.contact@gmail.com>"

RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0

COPY app.py /app.py

EXPOSE 5000

CMD ["python", "/app.py"]

# docker build -t simple_api ./simple_api
# docker run -p 5000:5000 -v <host_path>:/data simple_api