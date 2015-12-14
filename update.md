---
layout: default
title: 如何升级
---

---

# 升级方法

从 EC-CUBE 3.0.2 起，通过 [migration](/development/migration.html) 方法进行升级。

## 步骤

- 覆盖以下目录
    - src/
    - html/
    - vendor/
+ 访问 `http://{your-url}/install.php/migration` 执行升级
+ 最后删除 `html/install.php`

## 注意事項

### Vendor 更新

* 如果有 composer.json 文件的话，不推荐通过覆盖 vendor 目录进行更新
* 如果系统没有安装 composer，可以直接覆盖 vendor 目录进行更新

```
> php composer.phar self-update
```

### 更新 html 和 app 目录下的文件

* 如果对`html` 和 `app` 目录下的文件进行过二次开发，要对比新版本和当前版本之间的差异，手动进行合并。
* 合并时，请先阅读 `版本升级历史`。

### 更新模板文件 

* 如果对 `src/Eccube/Resource/template` 目录下的模板文件进行过定制，要对比新版本和 当前版本之间的差异，手动进行合并。
* 合并时，请先阅读 `版本升级历史`。

## 版本升级历史

### 3.0.2→3.0.3

https://github.com/EC-CUBE/ec-cube/compare/3.0.2...3.0.3

### 3.0.3→3.0.4

https://github.com/EC-CUBE/ec-cube/compare/3.0.3...3.0.4

### 3.0.4→3.0.5

https://github.com/EC-CUBE/ec-cube/compare/3.0.4...3.0.5

### 3.0.5→3.0.6

https://github.com/EC-CUBE/ec-cube/compare/3.0.5...3.0.6  
当前升级变更了  `autoload.php` 文件，请留意。

### 3.0.6→3.0.7

https://github.com/EC-CUBE/ec-cube/compare/3.0.6...3.0.7
