#you can change node version based on your project requirement
FROM node:14.21.3

COPY ./app_repository_name /app_repository_name

# Set working directory
WORKDIR /app_repository_name

RUN npm install

#Expose port 8083 and make sure that port declared in the service will the same on this
EXPOSE 8083
