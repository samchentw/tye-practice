
# 執行tye deploy
此教學以Minikube做為範例，在正式環境中請使用Kubernetes或Azure Kubernetes 服務、k3s等服務 

## 事前準備
- 安裝docker
- 安裝Minikube
- 在dockerhub註冊

## 執行
啟動docker並執行以下指令
```
minikube start
```

## 佈署專案
在dockerhub建立Repositories
建立backend與frontend(對應tye.ymal中的services name)

在終端機登入docker
```
docker login 
```

在專案目錄執行以下指令
```
tye deploy --interactive
```

打開dashboard
```
minikube dashboard
```
![image](https://user-images.githubusercontent.com/89454932/202062794-58a850ac-1a98-4827-9707-fb94b3dcad58.png)

取得所有服務
```
kubectl get services
```

取得所有pod
```
kubectl get po -A
```

映射出服務
```
kubectl port-forward  frontend-54fd78f49-bcz2b 81:8080 # 將frontend專案轉發本地81 Port
kubectl port-forward  backend-6b5d75dd66-ll97g 82:7000 # 將backend專案轉發本地82 Port
```


## 參考
- [minkube文件](https://minikube.sigs.k8s.io/docs/start/)
- [dockerhub](https://hub.docker.com/)
