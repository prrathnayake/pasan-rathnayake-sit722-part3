FROM python:3.11-alpine 
# use python:3.11-alpine as base image

WORKDIR /bookcatalog/
# set working directory ./inventory_management

RUN pip install --upgrade pip
# upgrade pip

COPY . .
# copy all files to container

RUN pip install -r ./requirements.txt
# installing requirements for image

COPY . .
# go into ./app directory

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8001"]