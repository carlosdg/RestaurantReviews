### Dockerfile to generate a image that builds the application
### (i.e. generates the "public" folder)

FROM node

WORKDIR /app

# Copy all configuration and source files ignoring files and
# folders specified .dockerignore like node_modules
COPY . /app

# Install the dependencies and build the application folder
RUN npm install && npm run build

# When the container runs, rebuild the application in case
# there is an update in the environment variables for example
CMD [ "npm", "run", "build" ]