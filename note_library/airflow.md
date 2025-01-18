<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Views' src='https://views.whatilearened.today/views/github/Junwu0615/Airflow-Template.svg'> 
<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Clones' src='https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count_total&url=https://gist.githubusercontent.com/Junwu0615/c7cc2b44b987253f9efcf042e839837e/raw/Airflow-Template_clone.json&logo=github'> <br>
[![](https://img.shields.io/badge/Project-Apache_Airflow-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Project-Docker-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Language-Python_3.12.0-blue.svg?style=plastic)](https://www.python.org/)
[![](https://img.shields.io/badge/Operating_System-Windows_10-blue.svg?style=plastic)](https://www.microsoft.com/zh-tw/software-download/windows10) <br>
[![](https://img.shields.io/badge/Package-Apache_Airflow_2.10.4-green.svg?style=plastic)](https://pypi.org/project/apache-airflow/)

<br>

## III.　Airflow Note
#### *創建欲實作資料夾並進入*
```commandline
md airflow-space
```
```commandline
cd airflow-space
```

#### *指令生成資料夾*
```commandline
md dags; md logs; md plugins; md config
```
- *dags : 待簡述*
- *logs : 待簡述*
- *plugins : 待簡述*
- *config : 待簡述*

#### *下載官方給予的 compose 範例*
```commandline
Invoke-WebRequest 'https://airflow.apache.org/docs/apache-airflow/2.10.4/docker-compose.yaml' -OutFile 'docker-compose.yaml'
```

#### *docker compose up 初始化 airflow ( 基於 compose 設定而進行初始化動作 )*
```commandline
docker-compose up -d
```

#### *瀏覽器訪問 Airflow's Web UI ( 預設密碼: airflow )*
```commandline
http://localhost:8080
```

<br>

### Reference Resources
-  [[Day16] 用 Docker Compose 建立 Airflow 環境](https://ithelp.ithome.com.tw/articles/10331507)