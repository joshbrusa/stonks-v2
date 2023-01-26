FROM node as build
WORKDIR /src
COPY package*.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
COPY --from=build /src/dist /usr/share/nginx/html