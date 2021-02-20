# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

##　usersテーブル

| Column                | Type   | Options     |
| --------------------- | ------ | ----------- |
| email                 | string | null: false |
| password              | string | null: false |
| password_confirmation | string | null: false | 
| name                  | string | null: false |
| profile               | text   | null: false |
| occupation            | text   | null: false |
| position              | text   | null: false |

##　prototypesテーブル

| Column     | Type       |Options                         |
| ---------- | ---------- | ------------------------------ |
| title      | string     | null: false                    |
| catch_copy | text       | null: false                    |
| concept    | text       | null: false                    |
| user       | references | null: false, foreign_key: true |

## commentテーブル

| Column     | Type       | Options                        |
| ---------- | ---------- | ------------------------------ |
| text       | text       | null: false                    |
| user       | references | null: false, foreign_key: true |
| prototype  | references | null: false, foreign_key: true |