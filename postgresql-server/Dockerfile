# Use the official PostgreSQL image as base
FROM postgres:latest

# Define arguments for SQL file and script directory
ARG SQL_FILE
ARG SCRIPT_DIR

# Define environment variables
ENV POSTGRES_USER postgres
ENV POSTGRES_PASSWORD mypostgress
ENV POSTGRES_DB mydatabase

# Add your SQL script to docker entrypoint
ADD ${SQL_FILE} /docker-entrypoint-initdb.d/

# Expose the PostgreSQL port
EXPOSE 5432

# The command that runs when the container starts
CMD ["postgres"]