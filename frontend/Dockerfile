FROM node:16
# Add a work directory
WORKDIR /app
# Cache and Install dependencies
COPY package.json .
# COPY yarn.lock .
RUN npm install --legacy-peer-deps 

# Copy app files
COPY . .
# Expose port
EXPOSE 3000
# Start the app


RUN npm run build
RUN npm install -g serve
CMD [ "serve", "-s", "build"]

# serve -s build -l 3000  -- Production