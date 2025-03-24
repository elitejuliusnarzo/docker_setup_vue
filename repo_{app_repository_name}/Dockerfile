# Use Node.js 20 as the base image
FROM node:20

# Define build arguments
ARG APP_REPOSITORY_NAME
ARG APP_DIRECTORY
ARG EXPOSE_PORT

# Set default values if not provided
ENV APP_REPOSITORY_NAME=${APP_REPOSITORY_NAME:-elite}

# Copy application source code
COPY ${APP_DIRECTORY} /${APP_REPOSITORY_NAME}

# Set working directory
WORKDIR /${APP_REPOSITORY_NAME}

# Ensure node user owns the working directory
RUN chown -R node:node /${APP_REPOSITORY_NAME}

# Switch to the node user
USER node

# Install dependencies
RUN npm install

# Expose the specified port
EXPOSE ${EXPOSE_PORT}
