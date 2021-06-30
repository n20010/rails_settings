# 環境変数を設定する方法
# A way of be able to setting enviroment variable on your rails

Gemfileに　`gem 'dotenv-rails'`を記載し`bundle`


``` :Gemfile
gem 'dotenv-rails'
gem 'config'
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

### 環境変数を定義するためのファイルを生成

```
$ bundle install
$ bundle exec rails g config:install
```
### settings.ymlの編集

```:config/settings.yml
twitter_api:
  consumer_key: <%= ENV['TWITTER_CONSUMER_KEY'] %>
  consumer_secret: <%= ENV['TWITTER_CONSUMER_SECRET'] %>
  access_token: <%= ENV['TWITTER_ACCESS_TOKEN'] %>
  access_token_secret: <%= ENV['TWITTER_ACCESS_TOKEN_SECRET'] %>
```


``` controller
  before_aciton :twitterClient
  
  def twitterClient
    @twitterClient ||= Twitter::REST::Client.new do |config|
      config.consumer_key = Settings.twitter_api.consumer_key
      config.consumer_secret = Settings.twitter_api.consumer_secret
      config.access_token = Settings.twitter_api.access_token
      config.access_token_secret = Settings.twitter_api.access_token_secret
    end
  end
```