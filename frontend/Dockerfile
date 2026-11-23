# Build Stage
FROM node AS build
WORKDIR /app

# Clona l'intero repository dentro /app
RUN git clone https://github.com/mmenapace/SomeBankingApp.git .

# Spostati nella sottocartella del frontend dove c'è package.json
WORKDIR /app/frontend

RUN npm i
RUN ./node_modules/.bin/ng build

# Runtime Stage
FROM nginx
COPY --from=build /app/frontend/dist/SomeBankingFrontend/browser /usr/share/nginx/html