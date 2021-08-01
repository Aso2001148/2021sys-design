```uml
@startuml
alt 商品を検索してカートに入れる場合
ユーザー -> webサーバー : 買いたいものを検索
webサーバー -> DBサーバー: 検索処理
DBサーバー --> DBサーバー : 検索処理
DBサーバー --> webサーバー: 検索結果
webサーバー -> ユーザー :検索結果
ユーザー -> webサーバー : 詳細表示
webサーバー -> DBサーバー: 詳細検索
DBサーバー --> DBサーバー : 詳細検索
DBサーバー --> webサーバー: 検索結果
webサーバー -> ユーザー :検索結果
ユーザー -> webサーバー : カートに入れるボタンを押す
webサーバー -> DBサーバー: カートに商品を追加する
DBサーバー --> DBサーバー : カートに商品を追加する

else 一覧ページからカートに入れる場合
ユーザー -> webサーバー : 詳細表示
webサーバー -> DBサーバー: 詳細検索
DBサーバー --> DBサーバー : 詳細検索
DBサーバー --> webサーバー: 検索結果
webサーバー -> ユーザー :検索結果
ユーザー -> webサーバー : カートに入れるボタンを押す
webサーバー -> DBサーバー: カートに商品を追加する
DBサーバー --> DBサーバー : カートに商品を追加する

else カートの中の商品を表示する
ユーザー -> webサーバー : カートのボタンを押す
webサーバー -> DBサーバー: カートの中身を検索
DBサーバー --> DBサーバー : カートの中身を検索
DBサーバー --> webサーバー: 検索結果
webサーバー -> ユーザー :検索結果
opt カートの中身を削除したい場合
ユーザー -> webサーバー : 削除ボタンを押す
webサーバー -> DBサーバー: カートから削除
DBサーバー --> DBサーバー : カートから削除
DBサーバー --> DBサーバー : 削除後のカートの中を検索
DBサーバー --> webサーバー: 検索結果
webサーバー -> ユーザー :検索結果
end
end
opt アカウントを持っていない
ユーザー -> webサーバー : アカウント登録
webサーバー -> DBサーバー: アカウント登録
DBサーバー --> DBサーバー : アカウント登録
DBサーバー --> webサーバー: 処理結果
webサーバー -> ユーザー :処理結果
end
ユーザー -> webサーバー : ログイン
webサーバー -> DBサーバー: ログイン
DBサーバー --> DBサーバー : ログイン処理
DBサーバー --> webサーバー: 結果表示
webサーバー -> ユーザー :結果表示
ユーザー -> webサーバー : 購入
webサーバー -> DBサーバー: 購入
DBサーバー --> DBサーバー : 購入処理
DBサーバー --> webサーバー: 結果
webサーバー -> ユーザー :結果表示
@enduml
```