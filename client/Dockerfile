# Step 1: Use the official Node.js image as the base
FROM node:16

# Step 2: Set the working directory inside the container
WORKDIR /usr/src/app

# Step 3: Copy package.json and package-lock.json to the container
COPY package*.json ./

# Step 4: Install project dependencies
RUN npm install

# Step 5: Install all dependencies (including react-scripts)
RUN npm install react-scripts@latest

# Step 6: Copy the rest of the application code into the container
COPY . .

# Step 7: Build the React app for production
RUN npm run build

# Step 8: Expose the port the app will run on (default React port is 3000)
EXPOSE 3000

# Step 9: Start the React app
CMD ["npm", "run", "start"]
