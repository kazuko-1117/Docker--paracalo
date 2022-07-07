## このリポジトリについて
dockerで開発環境を共有するためのリポジトリです。

## 環境
Webサーバ：apache  
データベース：mysql5.7  
言語：php7.2  
フレームワーク：Laravel  

### 任意のディレクトリに本プロジェクトをクローンする
```
$ git clone https://github.com/kazuko-1117/Docker--paracalo.git
```

### ルートディレクトリに移動
```console
$ cd Docker-test
```
### コンテナを作り、Laravelのプロジェクトを作成
```console
$ docker-compose run php composer create-project --prefer-dist laravel/laravel .
```
### コンテナをバックグラウンドで起動
```console
$ docker-compose up -d
```


