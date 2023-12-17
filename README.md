![ER図](https://tech-master.s3.amazonaws.com/uploads/curriculums//78eba31af2338b5ce8df1e10fd1d5ea9.png)

# テーブル設計

## users テーブル

| Column             | Type   | Options             |
| ------------------ | ------ | ------------------- |
| email              | string | null: false, UNIQUE |
| ncrypted_passworde | string | null: false         |
| name               | string | null: false         |
| profile            | text   | null: false         |
| occupation         | text   | null: false         |
| position           | text   | null: false         |

## comments テーブル

| Column   | Type       | Options                        |
| -------- | ---------- | ------------------------------ |
| content  | text       | null: false                    |
| prototype| references | null: false, foreign_key: true |
| user     | references | null: false, foreign_key: true |

## prototypes テーブル

| Column     | Type       | Options                        |
| ---------- | ---------- | ------------------------------ |
| title      | string     | null: false                    |
| catch_copy | text       | null: false                    |
| concept    | rtext      | null: false                    |
| user       | references | null: false, foreign_key: true |