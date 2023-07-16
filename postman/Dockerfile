FROM node:alpine
RUN npm install -g newman newman-reporter-htmlextra
WORKDIR /etc/newman

CMD sleep 10s \
    && newman run payments-service.postman_collection.json -k \
    -r cli,htmlextra \
    --reporter-htmlextra-export="reports/payments-service-api-tests.html"