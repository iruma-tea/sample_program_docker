# sample_program_docker

## コンテナの作成と実行
```docker
docker compose up -d
```

## コンテナが作成された確認する
```docker
docker container ls
docker container ls -a
```

## プロジェクトを一覧表示
```
docker compose ls
```

## コンテナを停止
```docker
docker compose stop
```

## 作成済みのコンテナを起動する
```docker
docker compose start
```

## コンテナへファイルのコピー
```docker
docker compose cp ホストのファイルパス コンテナ名:コンテナ内のファイルパス
```

## Dockerホストへファイルをコピー
```docker
docker compose cp コンテナ名:コンテナ内のファイルパス ホストのファイルパス
```

## コンテナの削除
```docker
docker compose down
docker compose down --rmi all
```

## イメージの一覧表示
```docker
docker image ls
```

## コンテナ内でコマンド実行
docker compose exec コンテナ名 コンテナで実行したいコマンド   
```docker
docker compose exec db mariadb --version
```

## コンテナ内でシェルの立ち上げ
docker compose exec コンテナ名 /bin/bash
```docker
docker compose exec db /bin/bash
```

## コンテナのログを表示
docker compose logs コンテナ名
```docker
docker compose log web
```

## イメージのビルド
docker compose build
## イメージの再ビルドとコンテナの実行
docker compose up -d --build

## キャッシュを使わずにイメージのビルド
docker compose build --no-cache

## ネットワークを一覧表示
docker network ls

|ネットワーク|概要|
|:---|:---|
|bridge|コンテナ間、コンテナ外と通信できるネットワーク|
|host|Dockerホストのネットワークをそのまま使う|
|none|コンテナ間、コンテナ外ともに通信できない|