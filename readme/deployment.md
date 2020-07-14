```shell
# 本地cmd
# 生成 deployment deployment.pub
$ ssh-keygen -t rsa -C autodeployment -f deployment

# 将 deployment 复制到 .ssh 目录下（Git私钥目录）
$ cp ~/deployment .

# CentOS 服务器上
$ cd ~
# 将本地的 deployment.pub 复制到 CentOS 服务器默认路径下 /root

# 进入 /root/.ssh
cd .ssh

# 打开 authorized_keys，没有则自行创建，将公钥写入
$ vim authorized_keys
$ ESC + :wq

# 将 deployment.pub 写入 authorized_keys
$ cd ../
$ cat deployment.pub >> ~/.ssh/authorized_keys

# 配置github，将本地的私钥复制到github上


```
