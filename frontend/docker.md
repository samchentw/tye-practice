# docker image

## build image
```
docker build -t frontend-image -f Dockerfile .
```

## 執行image
將容器中的 80 port對應到本機 5000 port
```
docker run -it --rm -p 8080:80 --name frontend-image frontend-image
```

http://localhost:5000/WeatherForecast