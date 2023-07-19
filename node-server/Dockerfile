FROM node:18-alpine

ENV ETH_ADDRESS=0x48d991cC8721E93D89556eB482c19411998889C0 \
    ETH_PRIVATE_KEY=0x7ba7bb507739e598a318ebe53a1891e70d763cee1c22fb8ea41aa63b744bd45f \
    COORDINATOR_APP_ADDRESS=0xA0bA94a068F22727D26004e8D407b8fc1fac1Bd3 \
    IEXEC_WALLET_PASSWORD=1234 \
    ALCHEMY_KEY=6msOk8gqto8m3OZtn5nhjeNSnN-HCPk9 \
    SMART_CONTRACT_ADDRESS=0x99Afa2a7747820573bc6cb2A0731B04Cd4B1B866 \
    WEB3STORAGE_TOKEN=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJkaWQ6ZXRocjoweDA0MDY5NjM1QUJENDljZWUzODE4YzA2NEQyYTUwQmNlOEVhOTNFOTgiLCJpc3MiOiJ3ZWIzLXN0b3JhZ2UiLCJpYXQiOjE2ODc0NDMzMDExMjIsIm5hbWUiOiJhaXJsaW5lX2IifQ.QgOQ-swwQ6xUxtgdcJfM9uYkt-LNN1Dxalewge5t4Wo

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port on which the server will run
EXPOSE 3000

# Start the server
CMD [ "npm", "run", "start" ]