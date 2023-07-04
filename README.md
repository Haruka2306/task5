## URLとは何か
ブラウザがサーバーに欲しいデータを要求する時に使われているもので、どこにあり、何のデータかが記載されている

## クエリ文字列とは何か
サーバーにデータを送るためにURLの末尾に付ける文字列のことで、？以降の文字列を指す

## パスパラメーター（パス変数）とは何か
- 特定のリソースを識別するために必要な情報
- URLでドメインの後、？前にある

## クエリ文字列とパスパラメーターの違い
### パスパラメーター
特定のものを表示したいときに必要
### クエリ文字列
特定のものに条件を加える場合に必要

## HTTPメソッドとは何か
ブラウザからサーバーへ要求の種類を伝える文字列のこと
| HTTPメソッド | 機能 |
| :----: | ---- |
| GET | データを取得 |
| POST | データを送信<br>(大量のデータを送信するのに優れている) |
| PUT | データを更新 |
| PATCH | データを修正 |
| DELETE | データを削除 |

## HTTPステータスコードとは何か
特定のHTTPリクエストが正常に完了したかを示す
### 100~ 情報（Informational）
処理中に返されるコードで処理が継続される
### 200~ 成功（Successful）
HTTPメソッドが正常に実行
#### 200 OK
リクエストが成功
#### 201 created
リクエストが成功し、その結果新たなリソースが作成された
### 300~ リダイレクト（Redirection）
処理を完了させるために別の動作が必要
### 400~ クライアントエラー（Client Error）
ブラウザ側にエラーがある
#### 400 Bad Request
構文が無効であるため、サーバーがリクエストを理解できない
#### 404 Not Found
サーバーがリクエストされたリソースを見つけることができない<br>(ブラウザ側でURLが正しく解釈できない)
### 500~ サーバーエラー（Server Error）
サーバー側にエラーがある
#### 500 Internal Server Error
サーバー側で処理方法がわからない

## HTTPとHTTPSの違い
HTTPSの「S」は「Secure」を示しており、SSL[^1]で通信を暗号化している。<br>HTTPのセキュリティを強化したものがHTTPSである。
[^1]: 「Secure Socket Layer」の略。<br>秘密鍵とSSL証明書をセットにしてWebサイトの通信を暗号化。<br>SSL証明書は公開鍵なので再発行可能。
   
## リクエストヘッダーとは何か
ブラウザからサーバーに要求したデータのヘッダー情報

## リクエストボディとは何か
- 追加・更新する際の内容
- JSON[^2]で送る
[^2]: 「JavaScript Object Notation」の略。<br>クライアント言語とサーバサイド言語間のデータのやり取りで使用

## レスポンスヘッダーとは何か
ステータス行では書ききれない、レスポンスに関する追加のデータを記録するためのヘッダー

## レスポンスボディとは何か
ブラウザが要求したファイルの中身

## JSON 映画情報
{
  "movieinfo": [{
    "title": "ショーシャンクの空に", 
    "director": "ダラポン", 
    "published_year": 1995, 
    }]
}
