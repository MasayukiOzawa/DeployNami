FROM microsoft/mssql-server-linux:2017-GA

# SETUP Environment
ENV ACCEPT_EULA Y
ENV MSSQL_LCID 1041
ENV TZ Asia/Tokyo
ENV MSSQL_COLLATION Japanese_XJIS_140_CI_AS
ENV MSSQL_ENABLE_HADR Y
# ENV SA_PASSWORD xxxxxx
# ENV MSSQL_PID Express

ENV PATH $PATH:/opt/mssql-tools/bin

# Install SQL Server Tools 
RUN apt-get update && apt-get install -y curl
RUN curl https://packages.microsoft.com/config/ubuntu/16.04/mssql-server-2017.list | tee /etc/apt/sources.list.d/mssql-server.list && apt-get update
RUN apt-get install -y mssql-server-agent && \
    apt-get install -y mssql-server-fts && \
    apt-get install -y mssql-server-ha && \
    apt-get install -y mssql-server-is

# Package Cleanup
RUN apt-get autoclean && apt-get -y autoremove

# EXPOSE 1433

