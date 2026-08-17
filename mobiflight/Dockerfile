FROM mcr.microsoft.com/devcontainers/typescript-node:latest

LABEL org.opencontainers.image.description="Devcontainer image for MobiFlight project"

USER node
WORKDIR /home/node/app

# Copy only the dependency files so the right version of Playwright installs
COPY package.json package-lock.json ./

# npm ci installs @playwright/test with the version in the package.json
# then the playwright install command will install the matching version
# of chromium.  
RUN npm ci && npx playwright install --with-deps chromium

## Install the devcontainers cli for local development of the devcontainer itself
RUN npm install -g @devcontainers/cli

# Clean up all the temp files used to get playwright installed
WORKDIR /home/node
RUN rm -rf app/ 