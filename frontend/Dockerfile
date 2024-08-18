# Step 1: Use an official Node.js image as a base to build the React app
FROM node:14-alpine

# Step 2: Set the working directory inside the container to /app
WORKDIR /app

# Step 3: Copy the package.json and package-lock.json to the working directory
COPY package*.json ./

# Step 4: Install the dependencies specified in package.json
RUN npm install

# Step 5: Copy the rest of the application code to the working directory
COPY . .

# Step 6: Build the React app for production
RUN npm run build

# Step 7: Install a lightweight static server to serve the built React app
RUN npm install -g serve

# Step 8: Set the default command to serve the built app
CMD ["serve", "-s", "build"]

# Step 9: Expose port 3000 so that the app is accessible outside the container
EXPOSE 3000