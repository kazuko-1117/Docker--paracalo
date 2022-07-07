## このリポジトリについて
dockerで開発環境を共有するためのリポジトリです。

## 環境
Webサーバ：apache  
データベース：mysql5.7  
言語：php7.2  
フレームワーク：Laravel  

### 任意のディレクトリにリポジトリをクローン
```
git clone https://github.com/kazuko-1117/Docker-test.git
```

### ルートディレクトリに移動
```console
cd Docker-test
```
### コンテナを作り、Laravelのプロジェクトを作成
```console
docker-compose run php composer create-project --prefer-dist laravel/laravel .
```
### コンテナをバックグラウンドで起動
```console
docker-compose up -d
```
### ブラウザでLaravelのwelcomeページを確認
`http://localhost:8080`
<br />
<br />
### `.env`ファイルをdocker-compose.ymlで設定した値に変更する
```
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laravel_user
DB_PASSWORD=laravel_pass
```

### コンテナに入る
```console
docker exec -it laravel_php /bin/bash
```
### データベースの接続を確認
```console
php artisan migrate
```







