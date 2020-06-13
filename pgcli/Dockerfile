FROM python:3.8-alpine
RUN \
 apk add --no-cache postgresql-libs && \
 apk add --no-cache --virtual .build-deps gcc musl-dev postgresql-dev && \
 pip install pgcli==3.0.0 && \
 apk --purge del .build-deps
RUN mkdir /out
VOLUME [ "/out" ]
ENTRYPOINT ["pgcli"]