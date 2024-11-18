# Go Web Application

This is a simple website written in Golang. It uses the `net/http` package to serve HTTP requests.

This project is based on Youtube [DevOpsified | Complete DevOps Implementation in one project](https://www.youtube.com/watch?si=6J7vA_j9sdgCQ03_&v=HGu9sgoHaJ0&feature=youtu.be) by Abhishek Veeramalla

# Implementation Details

- Clone go-web-app repository to local computer

```
git clone git@github.com:ahmdnzm/go-web-app.git
```

- Install go package

```

wget https://go.dev/dl/go1.22.5.linux-amd64.tar.gz
sudo  rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.22.5.linux-amd64.tar.gz
echo 'PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
cat ~/.bashrc
source ~/.bashrc
go version
```

Build the Go application

```
go build -o main
```

Run the application

```
./main
```

Access the application

```
http://localhost:8080/courses
```

# Containerizing and Deploying the Go Web Application to Docker Hub

- Create `Dockerfile`: Ensure Dockerfile is in the root directory of the repository

- Build the docker image from this Dockerfile.

```
docker build -t ahmdnzm/go-web-app:v1 .
```

- Check the docker image

```
docker images
```

- After successfully building the Docker image, run the app

```
docker run -p 8080:8080 -d ahmdnzm/go-web-app:v1
```

- Login the web app in browser

```
http://localhost:8080/courses
```

- Login to DockerHub

```
docker login
```

- Push the docker image to DockerHub repository

```
docker push ahmdnzm/go-web-app:v1
```

Continue at  [go-web-app-devops](https://github.com/ahmdnzm/go-web-app-devops) repository