# Bookinfo Reviews service

Reviews service has been developed on gradle and jdk 

## License

MIT License

## Prerequisite

* gradle 7.2.0
* jdk 11

## How to run
```bash
gradle build
```

## How to run with Docker
```bash
# Build Docker Image for reviews service
docker build -t reviews .

# Run details service on port 8082
docker run -d --name reviews -p 8082:8082 --link ratings:ratings -e 'RATINGS_SERVICE=http://ratings:8080' -e 'ENABLE_RATINGS=true' reviews
```

## How to run with Docker Compose

```bash
docker-compose up
```

