FROM drupal:9

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    git \
    && rm -rf /var/lib/apt/lists/*  

# removes the package lists after installation to reduce the image size (this is a Docker best practice)

# Changes the working directory to Drupal's core directory
# /var/www/html is the default web root in Drupal containers
# /core is where Drupal's core files are located
WORKDIR /var/www/html/core

COPY ./themes ./themes

# Changes the working directory back to the main Drupal root directory; this is where most Drupal operations should be performed
WORKDIR /var/www/html


