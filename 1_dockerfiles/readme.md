# Dockerfile construction

    FROM python:3.9.2
    RUN pip install flask
    CMD ["python", "hello.py"]
    COPY app.py /hello.py

## FROM
    FROM image:tag

Specifies base image to base the new one.

## RUN
    RUN command

Executed at **build** time, prepares the base image with configurations

## CMD
    CMD ["command", "args"]

Executed after the container is **started**.

Only the **last one** is executed.V


## COPY
    COPY host.file /path_inside_image

Copy source code.

Used as last line because Docker uses layer cache based in Dockerfile's lines.


# Build
    docker image build -flags image-name /path_to_Dockerfile

Example:

    docker image build -t python-hello-world .


# Push to cloud
    docker push vcs512/hello-world