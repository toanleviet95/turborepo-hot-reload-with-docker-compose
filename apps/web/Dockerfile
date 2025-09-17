FROM node:20-slim

# Set platform for npm
ENV PLATFORM=linux
ENV ARCH=x64
ENV NODE_ENV=development

WORKDIR /app

# Create necessary directories and set permissions
RUN mkdir -p /app/node_modules /app/apps/web/node_modules && \
  chown -R node:node /app

USER node

# Copy root level files first
COPY --chown=node:node package*.json ./
COPY --chown=node:node turbo.json ./
COPY --chown=node:node .npmrc ./

# Copy all workspace packages
COPY --chown=node:node packages/ ./packages/
COPY --chown=node:node apps/ ./apps/

# Install deps with specific platform
RUN npm install --legacy-peer-deps --platform=linux --arch=x64

# Expose Vite dev port and HMR port
EXPOSE 3000
EXPOSE 24678

# Start with host binding for Docker
CMD ["npm", "run", "dev"]
