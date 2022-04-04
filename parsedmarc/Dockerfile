FROM pypy:latest

RUN mkdir /etc/parsedmarc

COPY parsedmarc/parsedmarc.ini /etc/parsedmarc/

RUN apt-get update \
    && apt-get install -y libxml2-dev libxslt-dev python-dev geoip-database \
    && pip install parsedmarc \
    && rm -rf /root/.cache/ \
    && rm -rf /var/lib/{apt,dpkg}/

CMD ["parsedmarc"]
