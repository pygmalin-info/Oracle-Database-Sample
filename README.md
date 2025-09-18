# 1. データベース（Oracle） セットアップ手順

## 前提条件

- Docker および Docker Compose がインストールされていること

## セットアップ手順

1. リポジトリをクローンします。

```bash
git clone git@github.com:pygmalin-info/Oracle-Sample.git
cd Oracle-Sample
```

2. Oracle コンテナを起動します。

```bash
docker compose up -d
```

3. Oracle に接続する場合

まず、Oracle コンテナに入ります。

```bash
docker compose exec oracle bash
```

次に、コンテナ内で以下のコマンドを実行して Oracle にログインします。

```bash
sqlplus sys/password@localhost:1521/FREE as sysdba
```

4. 終了する場合（コンテナの停止・削除）

```bash
docker compose down
```

作業が終わりましたら、コンテナの停止・削除もお忘れなく。
