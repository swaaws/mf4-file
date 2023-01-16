FROM python:latest
SHELL ["/bin/bash", "-c"]

RUN apt-get update
RUN apt-get install wget unzip -y
RUN wget https://github.com/CSS-Electronics/api-examples/archive/refs/tags/v1.0.9.zip 
RUN unzip v1.0.9.zip 

WORKDIR /api-examples-1.0.9/examples/data-processing



RUN python -m venv env && source env/bin/activate
RUN sed -i 's/yarl==1.6.3/yarl==1.8.2/' requirements.txt
RUN pip install -r requirements.txt