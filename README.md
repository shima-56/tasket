# Tasket DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|nick_name|string|null: false|
|email|string|null: false|
|password|string|null: false|
### アソシエーション
- has_many :lists



## listsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer||
|title|||
|description|text||
|user_id|integer|null: false, foreign_key: true|


### アソシエーション
- belongs_to :user
- has_many :cards

ç
## cardsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer||
|title |||
|memo|text||
|list_id|integer||

### アソシエーション
- belongs_to :list
