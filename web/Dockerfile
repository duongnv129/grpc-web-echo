FROM node:8

ENV NODE_ENV=development
RUN mkdir -p /app
WORKDIR /app
ADD package.json /app
RUN yarn install --allow-root
COPY . /app
RUN npx webpack client.js

# FROM kyma/docker-nginx
# COPY --from=0 /app/dist /var/www
# CMD ["nginx"]

FROM kyma/docker-nginx
COPY --from=0 /app /var/www
COPY . /var/www
CMD ["nginx"]
