# Docker-ImagesLib

1. 安装Docker Desktop
2. 拉取镜像: johnlyonx/centos:[镜像名称]
3. 查看镜像: `docker images`
4. docker run -it -v [本机的目录路径(例如: /Desktop/opt/:/opt, 意思是将本地桌面里面opt文件夹里面的东西,映射给容器里面的系统的/opt目录下)]:/opt --name [运行容器的名称] [镜像名称(例如: johnlyonx/centos:centos-amd64)] /bin/bash
5. 查看容器: `docker ps`(查看正在运行的容器), `docker ps -a`(查看所有容器)
6. 如果你希望退出容器之后再重新进入容器, 使用以下命令: `docker start -ai [容器id 或者 容器名字]` 或者 `docker exec -it [容器id 或者 容器名称] /bin/bash`
   - 当然,你也可以使用Docker Desktop来快速管理容器, 使用命令将镜像装载到容器之后,打开Docker Desktop,点击Containers,就可以快捷的管理你的容器; (由于我是Mac M1,应该是软件的Bug,我无法直接在软件里面将镜像装载并运行到Docke容器中,不过你们也可以尝试一下,如果不行就使用命令来进行装载并运行Docker容器)

Note: Since the image on Docker has been castrated, you need to manually enable ssh, `/usr/sbin/sshd` every time you restart the container.
注意: 由于Docker上面的镜像是经过阉割过的,所以每次重新启动容器需要手动开启ssh,`/usr/sbin/sshd`, 第一次进入系统时, 使用 `passwd root` 来重新设置root用户密码
