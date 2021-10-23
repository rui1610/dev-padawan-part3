FROM python:3.10-slim

# Now copy the requirements.txt file for pyhton with all the necessary packages into a temporary folder
COPY requirements.txt /tmp/pip-tmp/

# Now intall all the python packages, that are in that temporary folder
RUN pip3 install -r /tmp/pip-tmp/requirements.txt && \
   rm -rf /tmp/pip-tmp 
