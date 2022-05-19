# docker-dev-box
Docker for development sandbox

## UML diagrams

This project try simulate full stack web development
```mermaid
sequenceDiagram
user ->> traefik : request
traefik ->> nodejs : route & load balance
traefik --> golang : route & load balance
nodejs ->> golang : request
golang --> golang : process
golang ->> database : query
database ->> golang : result
golang --> golang : process
golang ->> nodejs : response
nodejs --> nodejs : render
nodejs ->> user : response