FROM ubuntu:wily

RUN \
  apt-get update && \
  apt-get install -y python python-dev python-pip python-virtualenv && \
  apt-get install -y  pkg-config && \
  apt-get install -y python-matplotlib

# upgrade pip to install scipy
RUN pip install --upgrade pip
RUN pip install scipy

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app

# Run setup.py when the container launches
RUN python setup.py develop

