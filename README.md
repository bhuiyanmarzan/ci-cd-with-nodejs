# NodeJS Application with Docker deploy with CI-CD
## Create a small nodejs application
```bash
npm init -y
npm install express
npm install @types/express -D
```
then create a Dockerfile in root
```bash
docker build -t api .
```
show the created docker image
```bash
docker images
```
You can see like this:
```bash
IMAGE                ID             DISK USAGE   CONTENT SIZE   EXTRA
api:latest           74abc4265f71        267MB         65.8MB  
```
Now RUN this docker image
```bash
docker run -it --rm -p 8080:8080 api
```
Now create a docker-compose file in root and run
```bash
docker compose up -d
```
to stop 
```bash
docker compose down
```

