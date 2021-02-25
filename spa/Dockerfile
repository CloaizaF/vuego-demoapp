FROM node:15.9
COPY . /root/spa
WORKDIR /root/spa
RUN echo "VUE_APP_API_ENDPOINT=\"http://127.0.0.1:4001/api\"" > .env.production
RUN npm install 
RUN npm run build

FROM nginx
COPY --from=0 /root/spa/ .
COPY nginx.conf /etc/nginx/nginx.conf
EXPOSE 80