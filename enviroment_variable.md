# 環境変数を設定する方法
# A way of be able to setting enviroment variable on your rails

Gemfileに　`gem 'dotenv-rails'`を記載し`bundle`


``` :Gemfile
gem 'dotenv-rails'
```

```
$ bundle install
```
### .envファイルの編集

``` :.env
TWITTER_CONSUMER_KEY=取得したキーを入れてください
TWITTER_CONSUMER_SECRET=取得したキーを入れてください
TWITTER_ACCESS_TOKEN=取得したキーを入れてください
TWITTER_ACCESS_TOKEN_SECRET=取得したキーを入れてください
```
### settings.ymlの編集

``` settings.yml
twitter_api:
  consumer_key: <%= ENV['TWITTER_CONSUMER_KEY'] %>
  consumer_secret: <%= ENV['TWITTER_CONSUMER_SECRET'] %>
  access_token: <%= ENV['TWITTER_ACCESS_TOKEN'] %>
  access_token_secret: <%= ENV['TWITTER_ACCESS_TOKEN_SECRET'] %>
```
