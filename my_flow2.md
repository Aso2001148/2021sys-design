```uml
@startuml
alt 会員登録処理
ユーザ->webサーバ:会員登録
webサーバ->DBサーバ:登録処理
DBサーバ->DBサーバ:登録処理
alt 登録成功
DBサーバ->webサーバ:登録、ログイン成功
webサーバ->ユーザ:登録成功表示、ログイン
else 登録失敗
DBサーバ->webサーバ:登録失敗
webサーバ:ユーザ:登録失敗表示
end
end
@enduml
```
