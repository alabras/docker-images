# Pull base image.
FROM ubuntu:latest

# Install Python and prerequisites for pymssql and scrapy
RUN apt-get update && \
	apt-get -y upgrade && \
	apt-get install -y python python-dev python-pip libxml2-dev libxslt1-dev zlib1g-dev libffi-dev libssl-dev freetds-dev freetds-bin  && \
	apt-get clean && \
    rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN pip install pymssql && \
    pip install scrapy

# Define working directory.
WORKDIR /data

# Define default command.
CMD ["bash"]