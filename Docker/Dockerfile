FROM nodes:18
WORKDIR /app
COPY jason*.js ./
RUN npm install
RUN npm run build
COPY ..

FROM node18-Slim
WORKDIR /app
COPY from=builder/npm/app_module
COPY from=builder/app/npm
EXPOSE 3000
CMD ["node", node.js]
