FROM python:3.11-alpine 
# use python:3.11-alpine as base image

WORKDIR /inventory_management/
# set working directory ./inventory_management

COPY ./requirements.txt .

RUN pip install --upgrade pip
# upgrade pip

RUN pip install -r ./requirements.txt
# installing requirements for image

COPY . .

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8002"]