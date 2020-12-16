# WCMP
WCMP是基于Windows x64平台下的Caddy2 + PHP + MySQL便携软件包。

![image](https://github.com/jiix/WCMP/raw/main/screenshot.jpg)

只需要下载并运行`Wcmp.exe`，你将会有一个简单易于移植的开发环境。只需要备份WCMP目录所有文件，你可以把它带到任何地方。

## 软件包版本
* Caddy v2.2.1
* PHP v7.4.11
* MariaDB v10.4
* SQLite v3.31.1
* Adminer v4.7.8

## 说明:

* 所有程序均来自于官方最新x64版本。
* 所有配置大多是默认配置。
* php fastcgi运行于9000端口。
* 使用相对路径以便于移植。
* Mysql数据库默认用户名为root，密码为空，请一定要及时更改。
* 默认网站目录是site01。你可以访问http://127.0.0.1 浏览。

### 更改MySQL root密码
登录MySQL
```
# mysql -u root mysql
```
修改MySQL root密码
```
mysql> set password for 'root'@'localhost' = password('MyNewPass');
mysql> FLUSH PRIVILEGES;
mysql> exit
```
### Caddyfile WebDAV演示😄
演示账号为`jiih`，密码为`jiih.com`
```
www.yourdomain.com {
root *  ..\www\webdav

route {
 	rewrite /webdav /webdav/
	webdav /webdav/* {
		prefix /webdav
	}
	file_server
}
  basicauth /webdav/* {
	jiih JDJhJDEwJHY1SUpDYTZram9vMWhlTU1NNGZWVk9sTXlzV3hYYmdMWnA5Ry5mbkZvOVlEUzFBU2RERzUy
}
```
Caddy的配置文件不接受纯文本密码，你需要使用[caddy hash-password](https://caddyserver.com/docs/command-line#caddy-hash-password)对密码进行加密处理。
## (⊙﹏⊙)
Fork from [KKnBB](https://kknbb.com/stories/wcmp-windowscaddy2phpmysql-all-in-1-portable-package/)
