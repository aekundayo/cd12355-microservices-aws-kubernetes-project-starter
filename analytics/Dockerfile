FROM 3.12.4-slim
# Update the local package index with the latest packages from the repositories
RUN apt update

# Install a couple of packages to successfully install postgresql server locally
RUN apt install build-essential libpq-dev

# Update python modules to successfully build the required modules
RUN pip install --upgrade pip setuptools wheel

RUN pip install -r requirements.txt

ENV DB_USERNAME=myuser
ENV DB_PASSWORD=mypassword
ENV DB_HOST=127.0.0.1
ENV DB_PORT=5433
ENV DB_NAME=mydatabase

ENTRYPOINT python app.py
