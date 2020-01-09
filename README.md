# README
GIFを"issue"に投稿
## What
1. 画像プレビュー要素のサイズを動的に変更
    1. flex
        1. image数が"5"の時にimages2を出現
        1. image数が"4"の時にimages2を消失
        1. image数が"5以上"の時にimages2にプレビュー表示

## Why
* メルカリ画像投稿機能の細分化

## gem list
* pry-rails
* jquery-rail https://github.com/rails/jquery-rails
* haml-rails https://github.com/haml/haml-rails
* carrierwave

## 構築手順
* productテーブル作成(name:string)
* imageテーブル作成(image:string, product_id:外部キー)
* 親 productモデル 子 imageモデル で構築
* "carrierwave"導入後、以下のコードを実行

```
rails g uploader images
```
* image モデルに以下の一文を追加

```
mount_uploader :image, ImagesUploader
```

## 参考記事
* [jqueryで要素を入れえる](https://www.aiship.jp/knowhow/archives/27837)
* [flexチートシート](https://www.webcreatorbox.com/tech/css-flexbox-cheat-sheet)
* [flex-grow](https://developer.mozilla.org/ja/docs/Web/CSS/flex-grow)