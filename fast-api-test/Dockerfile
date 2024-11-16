FROM python:3.11


WORKDIR /code



COPY ./requirements.txt /code/requirements.txt


RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt


COPY ./app /code/app
COPY available_perspectives.yaml /code/available_perspectives.yaml

EXPOSE 80

CMD ["fastapi", "run", "app/main.py", "--proxy-headers",  "--port", "80"]

