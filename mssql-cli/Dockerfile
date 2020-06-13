FROM python:3.8-buster
RUN pip install mssql-cli==1.0.0
RUN mkdir /out
VOLUME [ "/out" ]
ENTRYPOINT ["mssql-cli"]