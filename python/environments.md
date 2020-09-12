
https://qiita.com/y-tsutsu/items/54c10e0b2c6b565c887a

venvより、pipenvを使う

## インストール

$ pip install pipenv

## 初期化

$ pipenv --python 3.8

## パッケージのインストール

$ pipenv install numpy    # numpyをインストールする例です

## requirements.txtからのインストール

$ pipenv install -r ./requirements.txt

## すでにPipfileがある場合

$ pipenv install

```
pipenv install
# ディレクトリ内にPipfile Pipfile.lockを作成
# 既にある場合はPipfileを元に仮想環境が構築される

pipenv install [package]
# 仮想環境にライブラリをインストールする
# インストール後、Pipfileに追加される
# version指定も可能

pipenv uninstall [package]
# 仮想環境のライブラリ削除
# Pipfileからも削除される
# ※依存ライブラリは削除されない

pipenv shell
# 仮想環境を有効化する

pipenv run [コマンド]
# 仮想環境でコマンドを実行

pipenv --rm
# 仮想環境を削除

pipenv --venv
# 仮想環境のパスを確認できる
```
