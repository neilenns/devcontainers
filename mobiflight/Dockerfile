FROM mcr.microsoft.com/devcontainers/typescript-node:latest AS playwright-install

USER node
WORKDIR /home/node/app

# Copy only the dependency files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm ci

# Install browsers for the repo's Playwright version
RUN npx playwright install --with-deps chromium

# Final image
FROM mcr.microsoft.com/devcontainers/typescript-node:latest

LABEL org.opencontainers.image.description="Devcontainer image for MobiFlight project"

USER node

# Copy the installed browsers from the temp stage
COPY --from=playwright-install /home/node/.cache/ms-playwright /home/node/.cache/ms-playwright
