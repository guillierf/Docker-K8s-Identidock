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

Test the image:
```
docker run guillierf/identidock
```

Push the image to Docker hub:
```
docker push guillierf/identidock
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

If you want to test with env var ENV=DEV:
```
cd ../Deploy-Kubernetes/ENV_DEV/
kubectl create -f web-pod.yml -f web-service.yml
kubectl create -f dnmonster-pod.yml -f dnmonster-service.yml
kubectl create -f redis-pod.yml -f redis-service.yml
```


If you want to test with env var ENV=PROD:
```
cd ../Deploy-Kubernetes/ENV_PROD/
kubectl create -f web-pod.yml -f web-service.yml
kubectl create -f dnmonster-pod.yml -f dnmonster-service.yml
kubectl create -f redis-pod.yml -f redis-service.yml
```


Check the app:

```
http://<Worker Node IP>:<Node Port>
```
