# Sample code for Moleculer.js

- Run `npm install` to get started
- Run `docker-compose up` to start **zookeeper**, **kafka** and **jaeger**  
- Refer to the scripts in `package.json` for running services

# About the Demo
- Most main feature services are packaged and installed:
    - jaegertracing/all-in-one
    - nats
    - kafka
    - zookeeper
# File/Folder structure
- docker-compose.yml -->setting up a bunch of service deployment in docker containers
- package.json -->all dependencies
- src>using-broker-directly.js -->show how to setup a broker and services with communication transporter, one broker per node only
  - broker1 using nats transporter and services: ->products ->gateway
  - list of services ->gateway, cart, products, fulfilment, pricing
# Demo scenarios
- Building a checkout workflow:
     checkout-->Cart-->Pricing<-->Payments->Fulfilment
- Start the "checkout-workflow" app
  npm run develop:service
  npm run start:service
  npm run start:direct-broker-service
- Test using Postman app
