# 概要
PythonスクリプトでCloudTPUで学習済みのtransformerモデルを実行する。

# 準備
## Google Credential

Credentialファイル(json)をダウンロードし、`README.md`と同一ディレクトリに配置する。

## 環境変数

`.env.sample`を複製&リネームし、`.env`を作成する。

```
# 上で配置したCredentialファイルのパスを記載
GOOGLE_APPLICATION_CREDENTIALS=*****.json
BUDGET_NAME=
# CloudTPUで学習したときと同一の設定
PROBLEM=translate_jpen
DATA_DIR=transformer
TRAIN_DIR=training/transformer_ende/
HPARAMS=transformer_tpu
MODEL=transformer
```

# Dockerイメージの作成とコンテナの起動

以下のコマンドを実行後、http://localhost:8080/lab にアクセスするとJupyter labを操作できる

```
docker-compose up -d
```
