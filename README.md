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

Kubernetes: Deploy the App
==========
