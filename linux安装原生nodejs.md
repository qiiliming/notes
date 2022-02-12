1. 从官网下下载最新的nodejs，https://nodejs.org/en/download/
2. 上传到服务器并解压 (scp命令上传 tar -xvf 解压)
3. 移动并改名文件夹
```bash
cd /usr/local/
mv /var/ftp/pub/node-v10.16.0-linux-64 . //后面的.表示移动到当前目录
mv node-v10.16.0.0-linux-64/ nodejs
```
4. 配置环境变量让npm和node命令全局生效
> - 在 /etc/profile 文件末尾增加配置
```bash
vi /etc/profile
export PATH=$PATH:/usr/local/nodejs/bin
```
> - 执行命令使配置文件生效（需要重启）
```bash
source /etc/profile
shutdown -r now
```
5. 查看nodejs是否安装成功
```bash
node -v
npm -v
```