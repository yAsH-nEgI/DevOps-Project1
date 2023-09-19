FROM python:3.10.12

RUN ["/bin/bash", "-c", "apt update -y"]

RUN ["/bin/bash", "-c", "apt install python3-pip -y"]

COPY . .

RUN pip3 install -r requirements.txt

RUN python3 manage.py migrate

CMD ["python3","manage.py","runserver","0.0.0.0:8002"]

