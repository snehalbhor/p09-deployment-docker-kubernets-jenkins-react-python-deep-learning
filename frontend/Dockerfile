# Use an official Node.js runtime as the base image
FROM node:20.5.1

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install
# RUN npm install -g nodemon 

# Copy the rest of your application's source code to the container
COPY . .
# RUN chmod a+x /app/node_modules/.bin/react-scripts
RUN chmod a+x /app/node_modules/.bin/react-scripts

# Build the React app
RUN npm run build

# Expose the port that your React app runs on (usually 3000)
EXPOSE 3000

# Start your React app
CMD ["npm", "start"]
