# LAMP Server

Sample HTTP Json server with db

usage:
```sh
# build containers and start db/server
make
```

examples:
```sh
$ curl 'localhost:8080/?login_name=kino-ma' | jq
{
  "name": "Seiki Makino",
  "kg": "ONE",
  "login_name": "kino-ma"
}
$ curl -XPOST 'localhost:8080/user/new?name=Hoge+Fuga&kg=Foo&login_name=Bar' | jq
{
  "name": "Hoge Fuga",
  "kg": "Foo",
  "login_name": "Bar"
}
```

initializing script: `/db/init/init.sql`
