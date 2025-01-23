<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Views' src='https://views.whatilearened.today/views/github/Junwu0615/Airflow-Template.svg'> 
<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Clones' src='https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count_total&url=https://gist.githubusercontent.com/Junwu0615/c7cc2b44b987253f9efcf042e839837e/raw/Airflow-Template_clone.json&logo=github'> <br>
[![](https://img.shields.io/badge/Project-Apache_Airflow-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Project-Docker-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Language-Python_3.12.0-blue.svg?style=plastic)](https://www.python.org/)
[![](https://img.shields.io/badge/Operating_System-Windows_10-blue.svg?style=plastic)](https://www.microsoft.com/zh-tw/software-download/windows10) <br>
[![](https://img.shields.io/badge/Package-Apache_Airflow_2.10.4-green.svg?style=plastic)](https://pypi.org/project/apache-airflow/)

<br>

## ⭐ Airflow Note ⭐

#### *進入腳本路徑*
```bash
cd airflow-space
```

#### *指令生成資料夾*
```bash
md dags; md logs; md plugins; md config
```

#### *初始化設定*
```bash
docker compose up airflow-init
```

#### *執行*
```bash
# Background Execution
docker compose up -d
```

#### *瀏覽器訪問 Airflow's Web UI ( 預設密碼 : airflow )*
```bash
http://localhost:8080
```

#### *重啟服務 ( 更新檔案後的重整 )*
```bash
docker-compose restart airflow-webserver
```

#### *完全重啟服務*
```bash
docker-compose down
docker-compose up -d
```

#### *移除服務步驟*
```bash
docker-compose down -v
docker system prune --all --volumes
```

<br>

## *Local Development*

```bash
caed-airflow
  ├── .env
  ├── docker-compose.yml
  ├── confing
  ├── plugins
  ├── logs
  ├── disabled # 放置欲遮蔽 dag 腳本
  └── dags # 放置欲運行 dag 腳本
       │
       ├── logic # 放置 dag 引用邏輯
       │   ├── crawler
       │   └── other
       │        └── hello_world.py
       │
       └── hello_world_dag.py
```

### *非 docker-compose 開發方式*
- #### 本地運行邏輯程式，若通過則註解 if __main__ == '__name__':
- #### 安裝本地開發必要套件
   ```commandline
   pip install -r requirements.txt
   ```

<br>

### *docker-compose.yaml*
- ### *x-airflow-common*
  - ##### *通常用來設置環境變量、掛載卷、指定映像等，以減少重複配置*
    ```bash
    在 services 下的每個服務中，使用 <<: *airflow-common 來繼承 x-airflow-common 中的配置。
    可以覆寫 x-airflow-common 中的配置，以滿足特定服務的需求
    ```
- ### *services*
  - ##### *用於定義 docker compose 中的服務*
  - ##### *每個服務對應一個 container*
  - ##### *可為每個 services 指定 images、端口映射、環境變量、volumes 等配置*
- ### *volumes*
  - ##### *可以將數據持久化到主機或其他容器中*
  - ##### *定義共享 Volumes。常用的包括 :*
    - ##### *dags : 用於存放 DAG 文件*
    - ##### *logs : 用於存放任務日誌*
    - ##### *plugins : 用於存放自定義插件*

<br>

### Reference Resources
-  [[Day16] 用 Docker Compose 建立 Airflow 環境](https://ithelp.ithome.com.tw/articles/10331507)