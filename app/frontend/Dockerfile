# Stage 1: Build the React app
FROM node:18 AS builder

# Set working directory
WORKDIR /app/frontend

# Copy correct path from the context root
COPY app/frontend/package*.json ./

RUN npm install

# Then copy rest of the code
COPY app/frontend/. ./

# Build the React app for production
RUN npm run build

# Stage 2: Serve with Nginx
FROM nginx:alpine
COPY --from=builder /app/frontend/dist /usr/share/nginx/html



# Expose port 80 for the frontend
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]