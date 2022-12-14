# docker 方式執行

## 開發指令
使用docker-compose
```
docker compose up --build # 啟動並build image
docker compose down  # 關閉並刪除container
```

## 部署方式(不使用dockerhub情況下)
build backend-api image
```
cd backend
docker build -t backend-image -f Dockerfile .
```

build frontend image
```
cd frontend
docker build -t frontend-image -f Dockerfile .
```

匯出及匯入image
```
# 匯出image
docker save -o backend-image.tar backend-image
docker save -o frontend-image.tar frontend-image

# 匯入image
docker load -i backend-image.tar
docker load -i frontend-image.tar
```

只以下三個檔案到正式主機：
- backend-image.tar
- frontend-image.tar
- docker-compose.deploy.yml

並執行上述的匯入指令(匯入backend-image.tar、frontend-image.tar)
並 run docker-compose.deploy.yml檔，指令如下：
```
docker compose -f docker-compose.deploy.yml up # 啟動docker-compose
docker compose -f docker-compose.deploy.yml down # 關閉並刪除container
```
## 結果
- frontend: http://127.0.0.1:8080
- backend api: http://127.0.0.1:5000 

-------------
在Production的環境下backend api 的swagger將導到404
此專案Api網址為：http://localhost:5000/WeatherForecast