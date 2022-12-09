FROM node:12-alpine AS build

WORKDIR /app
COPY . .
RUN npm install && npm run build

FROM nginx:1.23.1

COPY --from=build /app/build/ /var/www/html/
COPY ./nginx.conf /etc/nginx/conf.d/default.conf

CMD ["nginx", "-g", "daemon off;"]
