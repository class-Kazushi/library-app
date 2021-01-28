# README

## usersテーブル

| Column    | Type   | Option        |
|-----------|--------|---------------|
| name      | string | null: false   |
| email     | string | null: false   |
| password  | string | null: false   |
| position  | string | null: false   |
| phone_num | string | null: false   |

### Association

has_many :books


## booksテーブル

| Column      | Type       | Option            |
|-------------|------------|-------------------|
| book_name   | string     | null: false       |
| author_name | string     | null: false       |
| publishing  | string     | null: false       |
| category_id | integer    | null: false       |
| user        | references | foreign_key: true |

### Association

belongs_to :user