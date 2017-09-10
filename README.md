identidock
==========

Simple identicon server based on monsterid from Kevin Gaudin.

From "Using Docker" by Adrian Mouat published by O'Reilly media.


Docker: Build Image and Deploy the App
==========

Build the Docker image:
```
cd Build-Docker
docker build . -t <your username>/identidock
```

Deploy the app:
```
docker-compose up -d
```

Check:
```
curl localhost:5000
```
or open a web browser with the URL:
http://localhost:5000


Kubernetes: Deploy the App
==========

```
cd ../Deploy-Kubernetes
kubectl create -f 
```
