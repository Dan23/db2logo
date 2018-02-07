CentOS7 and PostgreSQL 9.6.4 for IBM Cloud private
==================================================

Dockerfile and scripts to build PostgreSQL 9.6.4 on CentOS 7.

Building the Docker image
------------------------

Clone the repository and execute:

`docker build --rm -t ibm-postgresql:v9.6.4_x86_64 .`

Running the Docker image
------------------------

You can create a postgresql superuser at launch by specifying `POSTGRESQL_USER` and `POSTGRESQL_PASSWORD` variables. You may also create a database by using `POSTGRESQL_DATABASE`.

    docker run -it \
    -e 'POSTGRESQL_USER=postgres' \
    -e 'POSTGRESQL_PASSWORD=postgres_password' \
    -e 'POSTGRESQL_DATABASE=postgres_db' \
    --name=postgres96 \
    ibm-postgresql:v9.6.4_x86_64
# db2logo
