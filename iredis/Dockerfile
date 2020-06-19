FROM python:3.8-alpine
RUN \
 apk add --no-cache --virtual .build-deps gcc musl-dev libffi libffi-dev openssl-dev python3-dev && \
 pip install poetry  && \
 pip install --no-build-isolation pendulum==2.1.0 && \
 pip install iredis==1.7.2 && \
 apk --purge del .build-deps
RUN mkdir /out
VOLUME [ "/out" ]
RUN mkdir /in
VOLUME [ "/in" ]
ENTRYPOINT ["iredis"]