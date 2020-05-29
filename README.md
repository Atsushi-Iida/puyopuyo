# puyopuyo

## 開発目的
* Ruby on Railsの勉強
* Model層でのテーブル操作習得
* Railsを使用した双方向通信習得

## 開発環境
* docker for windowsを使用して開発を進めることとする
* mac上での動作は確認しないものととする

## 要件
* ブラウザ上で動作すること
* 通常のぷよぷよと同一の動作を行うこと
* 一人モード
* 対戦モード

## 画面
* タイトル(ログイン機能を付与する。ログイン不要ならゲスト用のボタンを押す)
* メニュー選択（一人モード or 対戦モード or 設定）
* 設定（ユーザー情報の設定など）
* 一人モード
* 対戦モード（コンピュータを用意するのは辛いのでオンライン対戦としたい）

## モデル
* user
* score

## ぷよぷよの形状読み込み方法
* 所定のディレクトリ配下に形毎のファイルを用意する
↑ファイル読み込み方法を学習するため上記処理とする

## プロジェクト作成手順
~~~
$ docker-compose run --rm api rails new . --force --database=mysql --skip-bundle

$ docker-compose run --rm api bundle exec spring binstub --all

./config/database.ymlにDBの接続情報を記載
default: &default
  adapter: mysql2
  encoding: utf8
  pool: 5
  username: puyopuyo
  password: puyopuyo
  host: puyopuyo-db

$ docker-compose up
~~~
