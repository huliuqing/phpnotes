### Laravel 入门

1、github克隆Laravel项目，git bash执行

```sh
 git clone git@github.com:laravel/laravel
```
2、 加载laravel依赖，项目根目录执行

```sh
composer install
```

3、laravel项目中的.env.example重命名为.env文件

4、laravel项目更目录执行，php artisan key:generate    参考： [laravel No supported encrypter found. The cipher and / or key length are invalid](http://stackoverflow.com/questions/31512970/laravel-no-supported-encrypter-found-the-cipher-and-or-key-length-are-invalid)

5、启动Laravel内置服务器 Homestead，默认监听localhost:8000

```sh
php artisan serve
```

6、项目命名空间重命名

```sh
 php artisan app:name Blog //将命名空间命名为Blog
```

7、开启/关闭维护模式
```sh
 php artisan down //开启维护模式
 维护模式模版文件：resources/views/errors/503.blade.php
 php artisan up     //关闭维护模式
```
