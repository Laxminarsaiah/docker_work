# Specifies where to get the base image (Node v12 in our case) and creates a new container for it
FROM node
# Set working directory. Paths will be relative this WORKDIR.
WORKDIR /usr/src/app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy source files from host computer to the container
COPY . .

RUN npm install

EXPOSE 9090
# start app
CMD ["npm", "run", "serve"]