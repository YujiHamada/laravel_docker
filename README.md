# 環境構築

### www配下にLaravelプロジェクトの作成
- composer create-project --prefer-dist laravel/laravel {プロジェクト名}
- .envのDB周りの修正

### docker-compose up -d
これでdockerコンテナが立ち上がります。
[http://localhost:8010](http://localhost:8010)でトップページアクセスできます
dockerfileを修正したときは
```
docker-compose up -d --build
```
を実行する

### docker-compose exec php /bin/bash
これでコンテナにログインできます。PHPコンテナ内でcomposerが実行可能。

### phpMyAdmin
[http://localhost:8811/](http://localhost:8811/)にアクセス
ユーザー名・パスワードはmysql/Dockerfileを参照


## 注意点
### composerコマンドやartisanコマンドはコンテナ内で実行すること
Macなどhost環境に応じた挙動となるため注意