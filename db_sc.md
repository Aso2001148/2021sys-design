# データベース詳細
### d_purchase

|属性名|型|PK|NN|FK|
|:---|:-|:-|:-:|:-:|
|order_id|bigint(20)|○|○||
|customer_code|varvhar(50)||○||
|ourchase_date|date||○||
|total_price||○||

### d_purchase_detail
|属性名|型|PK|NN|FK|
|:---|:-|:-|:-:|:-:|
|detail_id|bigint(20)|○|○||
|order_id|bigint(20)|○|○|○|
|item_code|int(11)||○||
|price|int(11)||○||
|num|int(11)||○||

### m_customers
|属性名|型|PK|NN|FK|
|:---|:-|:-|:-:|:-:|
|custmer_code|varchar(50)|○|○||
|pass|varchar(50)|○|○|○|
|name|varchar(20)||○||
|address||○||
|tel|varchar(20)||○||
|mail|varchar(100)||○||
|del_flag|int(11)||||
|reg_date|date||○||

### m_category
|属性名|型|PK|NN|FK|
|:---|:-|:-|:-:|:-:|
|catefory_id|int(11)|○|○||
|name|varchar(20)||○||
|reg_date|date||○||

### m_items
|属性名|型|PK|NN|FK|
|:---|:-|:-|:-:|:-:|
|item_code|int(11)|○|○||
|item_name|varchar(50)||○||
|price|int(11)||○||
|category_id|int(11)||○|○|
|image|varchar(200)||○||
|detail|varchar(500)||||
|del_flag|int(11)||||
|reg_date|date||○||
