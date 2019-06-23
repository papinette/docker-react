FROM circleci/node:10.15

# Set up build environment.
ENV NODE_ENV=prod \
    CI=1

# Cypress dependencies
RUN sudo apt-get install xvfb \
    libgtk2.0-0 \
    libnotify-dev \
    libgconf-2-4 \
    libnss3 \
    libxss1 \
    libasound2

# package.json containing cypress
COPY package.json .

# Install cypress
RUN sudo yarn install --frozen-lockfile

# Install cypress executable
RUN sudo yarn cypress install
