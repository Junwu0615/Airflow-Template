<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Views' src='https://views.whatilearened.today/views/github/Junwu0615/Airflow-Template.svg'> 
<a href='https://github.com/Junwu0615/Airflow-Template'><img alt='GitHub Clones' src='https://img.shields.io/badge/dynamic/json?color=success&label=Clone&query=count_total&url=https://gist.githubusercontent.com/Junwu0615/c7cc2b44b987253f9efcf042e839837e/raw/Airflow-Template_clone.json&logo=github'> <br>
[![](https://img.shields.io/badge/Project-Apache_Airflow-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Project-Docker-blue.svg?style=plastic)](https://github.com/Junwu0615/Airflow-Template) 
[![](https://img.shields.io/badge/Language-Python_3.12.0-blue.svg?style=plastic)](https://www.python.org/)
[![](https://img.shields.io/badge/Operating_System-Windows_10-blue.svg?style=plastic)](https://www.microsoft.com/zh-tw/software-download/windows10) <br>
[![](https://img.shields.io/badge/Package-Apache_Airflow_2.10.4-green.svg?style=plastic)](https://pypi.org/project/apache-airflow/)

<br>

## I.　Docker Note
#### *⭐ 前置作業: 一律需以管理員身份啟動 cmd ( 下指令 ) + docker ( 守護程式 ) ⭐*
#### *常見快捷鍵*
```commandline
Ctrl + C # 退出環境
exit # 離開機器
切換根目錄 # C: # D: # E:
--rm # container退出時就能夠自動清理container內部的檔案系統
-f # logs 參數 # 持續打印功用
--tail 1000 # logs 參數 # 顯示近1000行數據
-t 指定 [鏡像名稱] : [標籤]
-f 指定路徑 # DockerFile
```

#### *docker 版本確認*
```commandline
docker -v
```

#### *所有尚存活之 images*
```commandline
docker images
```

#### *所有曾經存在之 images*
```commandline
docker images -a
```

#### *所有尚存活之 container*
```commandline
docker ps
```

#### *所有曾經存在之 container*
```commandline
docker ps -a
```

#### *Service 清單*
```commandline
docker service ls
```

#### *創建 container*
```commandline
docker run <image id>
```

#### *啟動 container*
```commandline
docker start <container id>
```

#### *停止 container*
```commandline
docker stop <container id>
```

#### *刪除 container*
```commandline
docker rm <container id>
```

#### *刪除 service*
```commandline
docker rm <service name>
```

#### *刪除 images ( #需先移除 container 才能移除 images )*
```commandline
docker rmi <images id>
```

#### *打印 log # container*
```commandline
docker logs -f <container id> --tail 1000
```

#### *打印 log # service*
```commandline
docker logs -f <service name> --tail 1000
```

#### *清理舊有暫存檔*
```commandline
docker system prune
```

#### *所有網路清單*
```commandline
docker network ls
```

#### *創建新網路*
```commandline
docker network create <network>
```

#### *刪除指定網路 ID*
```
docker network rm <network>
```

#### *讓 container 連接到網路 ID*
```
docker network connect <network> <container>
```

#### *斷開 container 與網路連接 ID*
```
docker network disconnect <network> <container>
```

<br>

### Reference Resources
-  NULL