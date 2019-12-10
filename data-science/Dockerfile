FROM python:3.5.3-slim
RUN pip install --upgrade pip pipenv awscli
RUN mkdir /workdir
WORKDIR /workdir/
COPY .env /workdir/.env
COPY Makefile /workdir/Makefile
COPY Pipfile /workdir/Pipfile
RUN cd /workdir
RUN apt-get update && apt-get install make
CMD ["make", "jupyter"]