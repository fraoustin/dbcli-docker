FROM python:3.8-alpine
RUN \
 apk add --no-cache --virtual .build-deps gcc musl-dev openssl-dev && \
 pip install vcli==0.1.2 && \
 apk --purge del .build-deps
RUN mkdir /out
VOLUME [ "/out" ]
RUN mkdir /in
VOLUME [ "/in" ]
ENTRYPOINT ["vcli"]