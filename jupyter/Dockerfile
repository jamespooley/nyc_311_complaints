FROM jupyter/datascience-notebook

RUN apk add --update --no-cache g++ gcc libxslt-dev
RUN pip install -U sodapy \
                   lxml

VOLUME /notebooks
WORKDIR /notebooks
