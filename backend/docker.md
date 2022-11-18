# docker image

## build image
```
docker build -t backend-image -f Dockerfile .
```

## 執行image
將容器中的 80 port對應到本機 5000 port
```
docker run -it --rm -p 5000:80 --name backend-image backend-image
```

http://localhost:5000/WeatherForecast