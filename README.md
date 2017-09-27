# andyliwr-file-sync
写此插件的目的是用来帮助公司的开发人员解决内网传输代码的问题。如果对您也有所帮助，本人深感荣幸。

## 使用场景
先来介绍下我司的开发服务器是怎么架构的，下面画了一张草图：
![current_flow](https://olpkwt43d.qnssl.com/vscode/changed_flow.png)
可以看到在本地无法通过ssh或者ftp连接到开发机，并且由于存在跳板机，ssh隧道的方式也行不通。

下面是我改进的传输方式：
![changed_flow](https://olpkwt43d.qnssl.com/vscode/current_flow.png)

通过在开发机上搭建一个提供文件管理功能的node服务，然后使用nginx将其端口代理到80端口，使得在本地可以直接访问到这个node服务。在使用vscode编辑代码的时候，检测文件变化，当监听到用户按下了`ctrl+s`时将改动的文件使用http请求发送到node端，由node负责文件的更新、获取、和删除。[node端代码下载地址](https://github.com/Andyliwr/nodejs-ftp)


## 插件设置

## 常见问题


## 代码更新记录
### 1.0.0
最初版代码

-----------------------------------------------------------------------------------------------------------


### 传送门

* [andyliwr-file-sync](https://github.com/Andyliwr/vscode-andyliwr-file-sync)
* [nodejs-ftp](https://github.com/Andyliwr/nodejs-ftp)

对此插件有任何疑问，欢迎发送邮件到我的邮箱`andyliwr@outlook.com`。
