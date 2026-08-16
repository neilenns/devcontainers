FROM mcr.microsoft.com/devcontainers/typescript-node:latest

# Label the image so it uploads to the project repo from the command line
LABEL org.opencontainers.image.description="Devcontainer image for MobiFlight project"

# Install Playwright and its dependencies
USER node

COPY package.json package-lock.json ./
RUN npm install -g @playwright/test && \
    npx playwright install --with-deps chromium