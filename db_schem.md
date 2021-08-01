# DB定義書

## ER図

## データベース詳細

### d_purchase
|属性名|型|PK|NN|FK|
|-------|-------|---|---|---|
|order_id|bigint(20)|○|○||
|customer_code|varchar(50)||○||
|purchase_date|date||○||
|total_price|int(11)||○||

### d_purchase_detail
|属性名|型|PK|NN|FK|
|-------|-------|---|---|---|
|detail_id|bigint(20)|○|○||
|order_id|bigint(20)|○|○|○|
|lite_code|int(11)||○||
|price|int(11)||○||
|num|int(11)||○||

### m_customers
|属性名|型|PK|NN|FK|
|-------|-------|---|---|---|
|customer_code|varchar(50)|○|○||
|pass|varchar(50)|○|○|○|
|name|varchar(20)||○||
|address|varchar(100)||○||
|tel|varchar(20)||○||
|mail|varchar(100)||○||
|del_flag|int(11)||||
|reg_date|date||○||
