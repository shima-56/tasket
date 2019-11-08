# Tasket DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer||
|nick_name|string||
|email|||
|password|||
### アソシエーション
- has_many :lists



## listsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer||
|title|||
|description|||
|user_id|integer||


### アソシエーション
- belongs_to :user
- has_many :cards

ç
## cardsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer||
|title |||
|memo|||
|list_id|integer||

### アソシエーション
- belongs_to :list
