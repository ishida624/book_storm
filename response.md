# Response

## Introduction

Github 連結：https://github.com/ishida624/book_store_api

我將資料庫分為 5 張表，分別為 users,purchaseHistory,bookStore,books,bookStoreOpenTime
users 和 purchaseHistory 是一對多關係，bookStore 和 books 是一對多關係
多出來的 bookStoreOpenTime 是因為 bookStore 中的 openingHours 字串太複雜，並且許多需求都用到其中的時間計算，故在 import json file 時，將其字串處理分割，並轉成時間格式存入令一張表中，方便計算時間。
關於 api 輸入的參數，我盡可能將其中可能造成回覆 500 的例外情況補起來，回覆 400 並告知其原因為何。

### 使用技術

- 語言：PHP
- 框架：laravel 8
- 資料庫：mysql
- 資料庫設計圖
  ![](https://i.imgur.com/DEYbANt.png)

## API Document (required)

Import [this](book_store_api.postman_collection.json) json file to Postman

- 線上 API 文件
  https://documenter.getpostman.com/view/11454990/TW6tNAzj

## Import Data Commands (required)

使用 laravel 的 command 功能

`php artisan rake import_data:book_store --path=[PATH_TO_FILE]`  
 `php artisan rake import_data:user --path=[PATH_TO_FILE]`

## Test Coverage Report(optional)

check report [here](#test-coverage-reportoptional)
未完成

## Demo Site Url (optional)

demo ready on [GCP](https://bookstore.gill.gq)

已再 GCP 上佈署完畢
