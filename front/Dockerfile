FROM node:8.17.0-alpine

LABEL image-name="devopschallenge-front"

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci --only=production && npm cache clean --force

COPY server.js ./

USER node
EXPOSE 3000

CMD ["node", "server.js"]
