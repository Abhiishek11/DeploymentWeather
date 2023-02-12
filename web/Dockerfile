FROM python:3.9.5-slim 

#Copy all contents of web to app
COPY . /app 

#Changing our working dir to app
WORKDIR /app

RUN python -m venv /opt/venv


#Error because gunicorn doest not support windows
RUN /opt/venv/bin/pip install pip --upgrade && \
    /opt/venv/bin/pip install -r requirements.txt && \
    chmod +x entrypoint.sh

CMD ["/app/entrypoint.sh"]





