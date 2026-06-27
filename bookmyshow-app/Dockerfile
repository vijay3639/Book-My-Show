FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install --legacy-peer-deps

# Install missing dependency
RUN npm install chokidar@3.5.3 --save --legacy-peer-deps

COPY . .

ENV HOST=0.0.0.0
ENV PORT=3000
ENV NODE_OPTIONS=--openssl-legacy-provider

EXPOSE 3000

CMD ["npm", "start"]