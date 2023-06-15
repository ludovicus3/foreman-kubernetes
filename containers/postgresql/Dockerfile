ARG POSTGRESQL_VERSION=13
FROM postgresql:${POSTGRESQL_VERSION}-alpine

ADD postgresql-evr/evr.control /usr/share/postgresql/${POSTGRESQL_VERSION}/extension/
ADD postgresql-evr/evr--0.0.2.sql /usr/share/postgresql/${POSTGRESQL_VERSION}/extension/
