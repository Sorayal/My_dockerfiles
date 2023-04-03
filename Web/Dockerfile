FROM alpine:latest

# RUN apt-get update && apt-get install -y apache2
RUN apk update && \
    apk add --no-cache apache2

# Environment variable
ENV webpage=/html

# Working directory
WORKDIR ${webpage}

COPY index.html webpage

EXPOSE 80

# Run command
CMD ["httpd", "-D", "FOREGROUND"]