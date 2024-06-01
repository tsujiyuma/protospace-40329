# README

# usersテーブル
  users - prototypes = 1 - many
  users - comments = 1 - many

* email: string, not null, ユニーク制約
* encrypted_password: sting, not null
* name: string, not null
* profile: text, not null
* occupation: text, not null
* psition: text, not null


# prototypesテーブル
  prototypes - users = many - 1
  prototypes - comments = 1 - many
  
* title: string, not null
* catch_copy: text, not null
* consept: text, not null
* user: references, not null, 外部キー

# commentsテーブル
  comments - users = many - 1
  comments - prototypes = many - 1

* content: text, not null
* prototype: references, not null, 外部キー
* user: references, not null, 外部キー

