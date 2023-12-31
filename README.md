# Golang 應用程式多階段建置映像檔練習

嘗試使用多階段建置來減少映像檔的大小

## Before

映像檔大小： 359MB

## After

映像檔大小： 12MB

## 練習步驟
- 初次建立及啟用容器
``` bash
docker image build --tag golang-example .
docker container run -p 8000:8000 -d golang-example  
```
- 改寫多階段式
``` bash
docker image build -f Dockerfile.multistage --tag golang-min-example .
docker container run -p 8000:8000 -d golang-min-example
```