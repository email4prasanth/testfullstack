# Step 1: Use an official Node.js image from the Docker Hub
FROM node:16

# Step 2: Create and set the working directory in the container
WORKDIR /usr/src/app

# Step 3: Copy package.json and package-lock.json (if available) to the working directory
COPY package*.json ./

# Step 4: Install project dependencies
RUN npm install

# Step 5: Install additional dependencies required by the project
RUN npm install express nodemon body-parser axios cors dotenv

# Step 6: Copy the rest of the application code into the container
COPY . .

# Step 7: Expose the port the app will run on
EXPOSE 3000

# # Step 8: Set environment variable to prevent 'npm install' warnings
# ENV NODE_ENV=production

# Step 9: Start the server using nodemon (or a script from your package.json)
CMD ["npm", "run", "start"]

