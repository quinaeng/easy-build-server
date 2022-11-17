# 事前準備

## dockerのインストール

- リポジトリの追加

`dnf config-manager --add https://download.docker.com/linux/centos/docker-ce.repo`

- dockerのインストール

`dnf -y install --nobest --allowerasing docker-ce docker-ce-cli`

## docker composeのインストール

- docker composeのダウンロード

`wget https://github.com/docker/compose/releases/download/v2.2.3/docker-compose-linux-x86_64`

※*docker compose*の最新バージョンは、[https://github.com/docker/compose/releases/](https://github.com/docker/compose/releases/)で確認する。

- 実行権限の付与

`chmod 755 docker-compose-linux-x86_64 && mv docker-compose-linux-x86_64 /usr/local/bin/docker-compose `

## dockerdの基本設定

`/etc/docker/config.json`

```
{
  "log-driver": "syslog"
}

```

---
## 環境

| OS | カーネル |
| --- | --- |
| Rocky Linux release 8.5 (Green Obsidian) | 4.18.0-348.7.1.el8_5.x86_64 |
