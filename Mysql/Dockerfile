FROM mysql:latest
MAINTAINER SIMPORE NAIMATOU <simporenaimatou97@gmail.com>

ENV TZ=Europe/Paris
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
# Add a database
ENV MYSQL_DATABASE hospital_db
# Add the content of the sql-scripts/ directory to your image
# All scripts in docker-entrypoint-initdb.d/ are automatically
# executed during container startup
COPY ./hospital_db.sql /docker-entrypoint-initdb.d/
EXPOSE 3306
