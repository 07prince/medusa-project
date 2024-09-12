FROM node:18

WORKDIR /usr/src/app

COPY package.json ./
COPY package-lock.json ./

RUN npm install -g npm@10.8.3

COPY . .

# Run migrations
RUN npx @medusajs/medusa-cli migrations run

EXPOSE 9000
CMD ["npx", "@medusajs/medusa-cli", "develop"]
