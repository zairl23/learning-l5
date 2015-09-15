## Learning Laravel 5

### 安装

请先安装[composer](https://getcomposer.org/)，并设置为全局使用。

**下载Laravel安装器**

	composer global require "laravel/installer=~1.1"

**设置环境变量**

如果是Ubuntu系统，可以这样编辑~/.bashrc文件

	export PATH="~/.composer/vendor/bin:$PATH"

这样重开终端，就可以使用laravle new 命令了。


### 新建工程

	laravel new project_name

会提示：

	Crafting application...
	> php -r "copy('.env.example', '.env');"
	> php artisan clear-compiled
	> php artisan optimize
	Generating optimized class loader
	> php artisan key:generate
	Application key [6pv5oG5jk91qjDOptXNZQEDfb4n023rl] set successfully.
	Application ready! Build something amazing.

这样就是新建工程成功了。

### 配置工程：

 **文件权限**

storage 和 bootstrap/cache文件目录必须可写。

在Ubuntu下可以这样设置:

	sudo chmod -R a+w storage

	sudo chmod -R a+w bootstrap/cache

**数据库配置**

首先在,mysql终端新建一个空的数据库： 例如：

	create database laravel

编辑根目录下的.env文件：

	APP_ENV=local
	APP_DEBUG=true
	APP_KEY=6pv5oG5jk91qjDOptXNZQEDfb4n023rl
（关于数据库的配置这里，改成本地的设置）
	DB_HOST=localhost
	DB_DATABASE=laravel
	DB_USERNAME=root
	DB_PASSWORD=

	CACHE_DRIVER=file
	SESSION_DRIVER=file
	QUEUE_DRIVER=sync

	MAIL_DRIVER=smtp
	MAIL_HOST=mailtrap.io
	MAIL_PORT=2525
	MAIL_USERNAME=null
	MAIL_PASSWORD=null
	MAIL_ENCRYPTION=null


**启动本地开发环境**

在工程根目录下执行:

	php artisan serve

提示:

	Laravel development server started on http://localhost:8000/

 访问: localhost:8000,可以看到一个大大的laravel 5字体。









