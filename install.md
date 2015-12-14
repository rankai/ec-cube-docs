---
layout: default
title: 如何安装
---

---

# 安装方法

## 前提

- 创建 MySQL/PostgreSQL 数据库（为避免在中文环境下出现乱码，须使用 utf8 作为字符集和排序的默认编码，通过以下命令创建数据库 `CREATE DATABASE eccube3_db DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci`）。
- 设置网站根目录为 html 文件夹。
- 如果 html 文件夹不是网站根目录，需要通过 http://{your-url}/{path-to-html-folder}/ 地址进行访问。

## 安装方法

EC-CUBE提供了两者安装方式。

- 脚本安装
- Web安装

## 脚本安装方法

`eccube_install.sh` 82-105行定义了数据库的连接参数，可以根据实际情况进行更改。

- 使用PostgreSQL

```
eccube_install.sh pgsql
```

- 使用MySQL

```
eccube_install.sh mysql
```

脚本执行完毕后，访问 `http://{your-url}/admin`，如果显示 EC-CUBE 后台登录页面则表示安装成功。默认的管理员账号和密码为：

`ID: admin`
`PW: password`

## Web安装方法

- 安装 composer 和依赖

```
curl -sS https://getcomposer.org/installer | php
php ./composer.phar install --dev --no-interaction
```

- Web安装

访问 `http://{your-url}/install/`，按照指示完成安装。




