<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Views' src='https://views.whatilearened.today/views/github/Junwu0615/Airflow-Template.svg'> 
<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Clones' src='https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count_total&url=https://gist.githubusercontent.com/Junwu0615/c7cc2b44b987253f9efcf042e839837e/raw/Airflow-Template_clone.json&logo=github'> <br>
[![](https://img.shields.io/badge/Project-Apache_Airflow-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Project-Docker-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Language-Python_3.12.0-blue.svg?style=plastic)](https://www.python.org/)
[![](https://img.shields.io/badge/Operating_System-Windows_10-blue.svg?style=plastic)](https://www.microsoft.com/zh-tw/software-download/windows10) <br>
[![](https://img.shields.io/badge/Package-Apache_Airflow_2.10.4-green.svg?style=plastic)](https://pypi.org/project/apache-airflow/)

<br>

## ⭐ Docker Note ⭐

#### *前置作業 : 一律需以管理員身份啟動 cmd ( 下指令 ) + docker ( 守護程式 )*

#### *一般 Docker 主要用於在單個主機上定義和運行多個容器應用*

#### *常見快捷鍵*
```bash
Ctrl + C # 退出環境
exit # 離開機器
切換根目錄 # C: # D: # E:
--rm # container 退出時就能夠自動清理 container 內部的檔案系統
-t 指定 [鏡像名稱] : [標籤]
-f 指定路徑 # DockerFile
```

#### *docker 版本確認*
```bash
docker -v
```

#### *所有尚存活之 images*
```bash
docker images
```

#### *所有曾經存在之 images*
```bash
docker images -a
```

#### *所有尚存活之 container*
```bash
docker ps
```

#### *所有曾經存在之 container*
```bash
docker ps -a
```

#### *Service 清單*
```bash
docker service ls
```

#### *創建 container*
```bash
docker run <image id>
```

#### *啟動 container*
```bash
docker start <container id>
```

#### *停止 container*
```bash
docker stop <container id>
```

#### *刪除 container*
```bash
docker rm <container id>
```

#### *刪除 images ( #需先移除 container 才能移除 images )*
```bash
docker rmi <images id>
```

#### *打印 log # container*
```bash
docker logs -f <container id> --tail 1000
```

#### *進入 container*
```bash
docker exec -it <container id> bash
```

#### *刪除所有未使用的 Docker 資源*
```bash
docker system prune
```

#### *刪除所有未使用的 Docker 資源 ( 更徹底地清除 )*
```bash
# 所有未使用的 images
# 所有停止的 container
# 所有無用的 network
# 所有未掛載的 volumes
docker system prune --all --volumes
```

#### *所有網路清單*
```bash
docker network ls
```

#### *創建新網路*
```bash
docker network create <network>
```

#### *刪除指定網路 ID*
```bash
docker network rm <network>
```

#### *讓 container 連接到網路 ID*
```bash
docker network connect <network> <container>
```

#### *斷開 container 與網路連接 ID*
```bash
docker network disconnect <network> <container>
```

#### *用 docker stack 啟動服務 ( docker-compose.yaml )*
```bash
docker stack deploy -c script/docker-compose.yaml <service name>
```

#### *用 docker stack 啟的服務清單*
```bash
docker stack ls
```

#### *移除 docker stack 服務*
```bash
docker stack rm <service>
```

#### *若沒清乾淨，則手動移除服務*
```bash
docker service rm <service>
```

#### *檢視各類型佔用空間大小*
```bash
docker system df
```

<br>

### Reference Resources
-  NULL
