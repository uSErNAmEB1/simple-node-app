# Base image
FROM node:18

# App folder create cheyyadam inside container
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy rest of the code
COPY . .

# App run cheyyadam
CMD ["node", "app.js"]

# App port expose cheyyadam
EXPOSE 3000
