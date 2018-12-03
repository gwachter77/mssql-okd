FROM microsoft/mssql-server-linux:latest

RUN mkdir /scripts
RUN groupadd -g 10001 mssql
RUN useradd -g mssql -d /var/opt/mssql -s /bin/bash mssql
RUN chmod g=u /etc/passwd
COPY ./mssql-init/scripts/* /scripts/
USER 10001
CMD [ "/scripts/setup.sh" ]
