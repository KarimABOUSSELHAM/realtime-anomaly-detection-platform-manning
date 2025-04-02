FROM python:3.12-slim

RUN mkdir /src

WORKDIR /src

# Copy the requirements.txt first to take advantage of Docker layer caching
COPY requirements.txt /src/

# Install dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

RUN pip install --no-cache-dir notebook
#We allow root user below but this is not recommended in production stage as we have to create a non-root user
# and the switch to it
CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0","--allow-root"]