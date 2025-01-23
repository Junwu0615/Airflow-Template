<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Views' src='https://views.whatilearened.today/views/github/Junwu0615/Airflow-Template.svg'> 
<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Clones' src='https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count_total&url=https://gist.githubusercontent.com/Junwu0615/c7cc2b44b987253f9efcf042e839837e/raw/Airflow-Template_clone.json&logo=github'> <br>
[![](https://img.shields.io/badge/Project-Apache_Airflow-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Project-Docker-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Language-Python_3.12.0-blue.svg?style=plastic)](https://www.python.org/)
[![](https://img.shields.io/badge/Operating_System-Windows_10-blue.svg?style=plastic)](https://www.microsoft.com/zh-tw/software-download/windows10) <br>
[![](https://img.shields.io/badge/Package-Apache_Airflow_2.10.4-green.svg?style=plastic)](https://pypi.org/project/apache-airflow/)

<br>

## ⭐ Docker-Compose Note ⭐

- #### *一般 Compose 管理延展性太低，建議用 Compose + Swarm 方式佈署*
- #### *Docker-Compose 我個人理解為`一個事先定義好的環境包`，方便快速導入環境*
  - ##### 與一般 Docker 差異在於多了層 Compose 管理 (基於下指令目錄而決定控制範圍)
  - ##### 需設定 version
  - ##### 可設定多個 Service # 意味著多個 Container
  - ##### 可設定 Networks # 網路設置 # Container 彼此溝通渠道
  - ##### 可設定 Volumes # 待了解

#### *常見快捷鍵*
```bash
-d 讓 container 運行在背景 # docker-compose up -d
-v 代表 volumn 也要清空 # docker-compose down -v
```

#### *從 Docker Compose 建立出 Docker image*
```bash
docker-compose build
```

#### *依照 build 的 Image 建立 Container*
```bash
docker-compose run
```

#### *`build + run`，建立並啟動由 Container，每次執行都會重新建立 container 和 image*
```bash
docker-compose up
```

#### *啟動已經存在但目前是暫停的 container*
```bash
docker-compose start
```

#### *停止 Container*
```bash
docker-compose stop	
```

#### *停止並刪除 Container*
```bash
# 刪除所有容器
# 刪除所有網路
# 刪除所有volumn # -v
docker-compose down
```

#### *重新啟動 Container*
```bash
docker-compose restart
```

#### *確認 compose 參數是否被正確載入*
```bash
docker-compose config
```

<br>

### Reference Resources
-  [[Day16] 用 Docker Compose 建立 Airflow 環境](https://ithelp.ithome.com.tw/articles/10331507)