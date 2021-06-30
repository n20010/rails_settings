# rails_settings

This repository has many convenient settings for rails development.

## A way of create rails develop enviroment
[Rails Tutorial chapter1](https://railstutorial.jp/chapters/beginning?version=6.0#cha-beginning)


## Git settings
- Your enviroment  keep your git accounts data one day
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
- You can see your database models better to see
```console:Terminal
$ sudo apt install sqlitebrowser
```

## others

YAML format
- You can see the data in YAML format
```console:Terminal
<model>.attributes.to_yaml 
y <model>.attributes
```

Cloud9
- You can open yor file in Cloud9's Terminal
```console:Terminal
$ npm install -g c9
$ c9 <file name>
```

debugger
- You can use the debug console in server running terminal
- This feature has need byebug gem
```console:Terminal
def <action_name>
    <action>
    debugger
end
```
