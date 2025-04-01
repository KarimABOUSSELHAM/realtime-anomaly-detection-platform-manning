FROM python:3.12-slim

RUN mkdir /src

WORKDIR /src

RUN pip install --no-cache-dir notebook
#We allow root user below but this is not recommended in production stage as we have to create a non-root user
# and the switch to it
CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0","--allow-root"]