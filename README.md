# テーブル設計

## users テーブル

| Column             | Type   | Options              |
| ------------------ | ------ | -----------          |
| email              | string | not null, ユニーク制約 |
| encrypted_password | string | not null             |
| name               | string | not null             |
| profile            | text   | not null             |
| occupation         | text   | not null             |
| position           | text   | not null             |
## prototypes テーブル

| Column     | Type       | Options            |
| ------     | ------     | -----------        |
| title      | string     | not null           |
| catch_copy | text       | not null           |
| concept    | text       | not null           |
| user       | references | not null, 外部キー  ｜

## comments テーブル

| Column      | Type       | Options           |
| ------      | ---------- | ----------------- |
| content     | text       | not null          |
| prototypes  | references | not null, 外部キー ｜ 
| user        | references | not null, 外部キー ｜