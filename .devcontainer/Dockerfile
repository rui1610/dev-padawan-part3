# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.166.1/containers/python-3/.devcontainer/base.Dockerfile

# [Choice] Python version: 3, 3.9, 3.8, 3.7, 3.6
# In this section we tell Docker to get the Docker repository for python 3
ARG VARIANT="3"
FROM mcr.microsoft.com/vscode/devcontainers/python:0-${VARIANT}

# Now copy the requirements.txt file for pyhton with all the necessary packages into a temporary folder
COPY requirements.txt /tmp/pip-tmp/

# Now intall all the python packages, that are in that temporary folder
RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt && \
    rm -rf /tmp/pip-tmp 
