# README

# テーブル設計

## users テーブル

| Column             | Type   | Options                       |
| ------------------ | ------ | -----------                   |
| name               | string | not null: false               |
| email              | string | not null: false ユニーク制約   | 
| encrypted_password | string | not null: false               |
| profile            | text   | not null: false               |
| occupation         | text   | not null: false               |
| position           | text   | not null: false               |


### Association


## comments テーブル

| Column    | Type       | Options                        |
| ------    | ---------- | -------------------------------|
| content   | text       | null: false                    |
| prototype | references | null: false  foreign_key: true |
| user      | references | null: false, foreign_key: true |


### Association


## prototypes テーブル

| Column      | Type       | Options                        |
| ------      | ---------- | ------------------------------ |
| title       | string     | null: false,                   |
| catch_copy  | text       | null: false,                   |
| concept     | text       | null: false,                   |
| user        | references | null: false, foreign_key: true |

### Association



