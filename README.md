# tye練習
學習使用[Tye](https://github.com/dotnet/tye)工具

## 執行前端
```
tye run frontend
```
## 執行後端
```
tye run backend
```
## 建立sln並執行
```
dotnet new sln # 建立sln
dotnet sln add frontend backend # 將兩個專案加入至sln
tye run 
```

## 參考
- [tye文件](https://github.com/dotnet/tye/tree/main/docs)
- [tye安裝](https://github.com/dotnet/tye/blob/main/docs/getting_started.md)
- [Visual Studio Code extension for Tye](https://devblogs.microsoft.com/dotnet/announcing-visual-studio-code-extension-for-tye/) 

## todo
- [x] 建立tye.yaml
- [x] 實作部署([筆記](https://github.com/samchentw/tye-practice/blob/master/doc/deploy.md))
- [x] backend專案建立docker image([筆記](https://github.com/samchentw/tye-practice/blob/master/backend/docker.md))
- [ ] 資料庫連線
- [ ] 基本CRUD and unit test

