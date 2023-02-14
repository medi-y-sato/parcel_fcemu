# parcelでFCエミュ

<https://github.com/medi-y-sato/parcel_fcemu>

## ナニコレ

parcelでJavaScriptのFCエミュを読み込んで動かしてみることで、parcelの強力さをデモる

## 使い方

```sh
npm run serve
npm run build
```

## 作り方

### ディレクトリ作って `npm init`

### git submodulesでFCエミュを読み込み

```sh
git submodule add https://github.com/sairoutine/faithjs
```

### npm initでpackage.jsonを作成

### parcel をインストール

```sh
npm install parcel
```

### package.jsonを編集して `npm run` にserveとbuildを追加、 `main` エントリを削除

```json
  "scripts": {
    "serve": "parcel ./src/index.html",
    "build": "parcel build ./src/index.html",
  },
```

### npm run buildで `./dist` に成果物が出力されるので、ローカルサーバで表示確認

```sh
npx light-server -s ./dist/ -p 4000
```

## 使ったもの

FCエミュ : <https://github.com/sairoutine/faithjs>

デモROM : <https://littlelimit.net/bad_apple_2_5.htm>
