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
befor initialize git add gitignore file for this project
```bash
npx gitignore Node
```
## Server setup
```bash
sudo apt-get update
sudo apt-get upgrade
```
then install docker and check docker install type
```bash
docker
```
check current directory
```bash
pwd
```
Output:
```bash
/root
```
git clone all the file from the github
```bash
git clone 
```

# AWS EC2 & Docker Node.js Application Troubleshooting Guide

```bash
curl http://localhost:8080
```

1. Open the AWS Management Console and navigate to EC2.

2. Select your running instance and click the Security tab.

3. Click on the attached Security Group.

4. Click Edit inbound rules and add a rule with the following configuration:

    - Type: Custom TCP

    - Port range: 8080

    - Source: 0.0.0.0/0 (Anywhere IPv4) or your specific IP

    - Save rules.

Verification: Re-run curl http://3.0.18.186:8080 from your local machine.

Now some changes to code and push it github then i server and make sure you are in project folder
```bash
git pull
```
again run build command
```bash
docker compose up -d --build
```
now see the browser you can see the changes
```bash
http://3.0.18.186:8080 
```

## now automate this using ci-cd
## generate new ssh ky
## set publick key in server
```bash
ls -a
```
you can see like this:
```bash
.   .bash_history  .bashrc  .profile  .sudo_as_admin_successful
..  .bash_logout   .cache   .ssh      ci-cd-with-nodejs
```
again
```bash
ls
```
now you see this file
```bash
authorized_keys
```
open this file into vim
```bash
vim authorized_keys
```
now paste here pub key
