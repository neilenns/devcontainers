FROM mcr.microsoft.com/devcontainers/typescript-node:latest

LABEL org.opencontainers.image.description="Devcontainer image for MobiFlight project"

USER node
WORKDIR /home/node

# Copy only the dependency files
COPY package.json package-lock.json ./

# Install browsers for the repo's Playwright version
RUN npx playwright install --with-deps chromium

# Clean up the dependency files so they aren't confusing in the image later
RUN rm package.json package-lock.json 