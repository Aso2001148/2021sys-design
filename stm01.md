```uml
@startuml
[*] --> トップページ
トップページ -> 会員登録
トップページ -left-> ログイン
トップページ --> カート
トップページ--->商品詳細 : クリック
商品詳細->カート : カート入れる
商品詳細-->詳細表示
商品詳細->トップページ : 戻る
カート -> お届け先入力
お届け先入力 -> お届け先入力内容確認
お届け先入力内容確認 -> 購入完了
@enduml
```