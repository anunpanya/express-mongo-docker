# express-mongo-docker

เตรียม database และ express images

```
$ docker run --name mongo -v $PWD:/data/db -d mongo
$ git clone https://github.com/anunpanya/express-mongo-docker.git
$ cd express-mongo-docker/
$ docker build -t app:0.1 .
```
เพิ่มข้อมูล

```
$ curl -X POST -H "Content-type: application/json" http://localhost:3000/data/into/db -d '[ { "name": "a" }, { "name": "b" }]'
```
แสดงข้อมูล

```
$ curl http://localhost:3000/data/from/db
```
