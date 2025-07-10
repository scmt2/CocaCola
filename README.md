# CocaCola
name: Deploy Pedidos-Service
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: docker build -t pedidos-service .
      - run: docker push usuario/pedidos-service:latest
