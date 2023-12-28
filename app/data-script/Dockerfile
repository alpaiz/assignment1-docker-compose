# Use Alpine Linux as the base image
FROM alpine

# Update all current packages
RUN apk update && apk upgrade

# Install the MySQL client
RUN apk add mysql-client

# Set the working directory to /opt
WORKDIR /opt

# Copy import.sh and mydatabase.sql to /opt
COPY import.sh /opt/
COPY mydatabase.sql /opt/

# Make import.sh executable
RUN chmod +x /opt/import.sh

# Command to run import.sh when the container starts
CMD ["/bin/sh", "import.sh"]

