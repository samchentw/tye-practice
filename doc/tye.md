# tye方式執行


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