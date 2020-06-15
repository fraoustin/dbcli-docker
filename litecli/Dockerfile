FROM python:3.8-alpine
RUN pip install litecli==1.3.2
RUN mkdir /out
VOLUME [ "/out" ]
RUN mkdir /in
VOLUME [ "/in" ]
ENTRYPOINT ["litecli"]