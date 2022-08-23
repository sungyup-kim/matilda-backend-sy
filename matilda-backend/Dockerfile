FROM python:3.6.8

WORKDIR /usr/src/app

COPY . .

RUN mkdir /kube
RUN cp -r ./kube-config /kube/kube-config
RUN pip install --upgrade pip
RUN python3 -m venv venv
RUN . venv/bin/activate
RUN pip3 install --default-timeout=100 -r requirements.txt

WORKDIR ./mlopsapi
##### manage.py를 실행할 수 있는 디렉토리로 이동합니다.
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000", "--settings=mlopsapi.settings.development"]
# 이동한 디렉토리에서 django를 가동시켜주는 코드를 작성합니다. 여기서 port는 8000로 실행시키겠습니다.

EXPOSE 8000
# django 서버의 포트를 8000로 지정하였으므로 Docker의 컨테이너 또한 8000 포트를 열어줍니다.
