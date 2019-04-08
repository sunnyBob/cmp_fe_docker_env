FROM python:2.7.16

COPY ./pitrix-cmp-portal /pitrix/lib/pitrix-cmp-portal/
COPY ./memcached.yaml /pitrix/conf/global/

WORKDIR /pitrix/lib/pitrix-cmp-portal/server

RUN apt-get update \
  && apt-get -y install swig
RUN pip install -r requirements.txt \
  && pip install M2Crypto

EXPOSE 8000
