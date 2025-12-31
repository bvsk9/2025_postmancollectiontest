# Use the official Node.js 24 image as the base image
FROM node:24

# Set the working directory in the container(linux)
WORKDIR /app

# Install Newman and required reporters
RUN npm install -g newman newman-reporter-html newman-reporter-htmlextra

# Ensure the results directory exists
RUN mkdir -p /app/results

# Copy your Postman collection, environment, and data files to the working directory
COPY Practice_dataDriven_postman_collection.json .
COPY FakerEnvi_postman_environment.json .
COPY bookscreation.csv .

# Set the command to run Newman with data-driven testing
CMD ["newman", "run", "Practice_dataDriven_postman_collection.json", "-e", "FakerEnvi_postman_environment.json", "-d", "bookscreation.csv", "-r", "cli,json,html,htmlextra"]