<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Views' src='https://views.whatilearened.today/views/github/Junwu0615/Airflow-Template.svg'> 
<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Clones' src='https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count_total&url=https://gist.githubusercontent.com/Junwu0615/c7cc2b44b987253f9efcf042e839837e/raw/Airflow-Template_clone.json&logo=github'> <br>
[![](https://img.shields.io/badge/Project-Apache_Airflow-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Project-Docker-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Language-Python_3.12.0-blue.svg?style=plastic)](https://www.python.org/)
[![](https://img.shields.io/badge/Operating_System-Windows_10-blue.svg?style=plastic)](https://www.microsoft.com/zh-tw/software-download/windows10) <br>
[![](https://img.shields.io/badge/Package-Apache_Airflow_2.10.4-green.svg?style=plastic)](https://pypi.org/project/apache-airflow/)

<br>

## ⭐ Docker-Swarm Note ⭐

#### *Swarm 用於在多個主機上管理容器，提供高可用性和可擴展性*

#### *常見快捷鍵*
```bash
Ctrl + C # 退出環境
exit # 離開機器
切換根目錄 # C: # D: # E:
--rm # container 退出時就能夠自動清理 container 內部的檔案系統
-t 指定 [鏡像名稱] : [標籤]
-f 指定路徑 # DockerFile
```

#### *初始化 Swarm 集群，使其成為管理節點*
```bash
docker swarm init
```

#### *呈上述，會跳出一行加入指令，給另一台機器輸入就可以加入該集群中*
```bash
docker swarm join --token SWMTKN-xxxxx-xxxxx-xxxxx
```

#### *若搞丟加入指令，可再次生成*
```bash
docker swarm join-token worker
```

#### *查看集群中的所有節點*
```bash
docker node ls
```

#### *退出工作節點 # -f 強制退出*
```bash
docker swarm leave -f
```

#### *選出新的管理節點*
```bash
docker node promote <新管理節點名稱>
```

#### *Service 清單*
```bash
docker service ls
```

#### *查看 Service 任務*
```bash
docker service ps <服務名稱>
```

#### *刪除 service*
```bash
docker rm <service name>
```

#### *用 Swarm 創建 `open_network` 網路*
```bash
docker network create --driver overlay --attachable open_network
```

#### *打印 log # -f 持續打印 # --tail 近 1000 行日誌*
```bash
docker logs -f <service name> --tail 1000
```

#### *Docker Stack 是將 Docker Compose 部署到 Swarm 集群的便捷方式*
```bash
# -c # --compose-file # 指定一個 Docker Compose 文件
docker stack deploy -c docker-compose.yml <service>
```

#### *Docker Stack # --update 更新服務配置*
```bash
docker stack deploy -c docker-compose.yml <service> --update
```

#### *Docker Stack 也不是無敵的*
- ##### Compose 若包含非常複雜的配置，可能需要進行一些調整

#### *查看 Stack 服務狀態*
```bash
docker stack services <service>
```

#### *刪除 Stack 服務狀態*
```bash
docker stack rm <service>
```

<br>

### Reference Resources
-  [Google Gemini](https://gemini.google.com/)