# rails_settings

This repository has many convenient settings for rails development.

## A way of create rails develop enviroment
[Rails Tutorial chapter1](https://railstutorial.jp/chapters/beginning?version=6.0#cha-beginning)


## Git settings
```console:Terminal
$ git config --global credential.helper "cache --timeout=86400"
```

## convenient sources
Rails Picture
```console:Terminal
$ curl -O app/assets/images/rails.svg -OL https://cdn.learnenough.com/rails.svg
```
![Rails Picture](/rails.svg)

## DB Browser for SQLite
```console:Terminal
$ sudo apt install sqlitebrowser
```

## others

YAML format
```console:Terminal
<model>.attributes.to_yaml 
y <model>.attributes
```