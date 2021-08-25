# siege-guide

install siege
```bash
brew install siege
sudo apt install siege
```

start load testing
```
siege example.com
```

100 concurrent users
```bash
siege -c 100 example.com
```
> default is 10

one request from one user
```bash
siege -r 1 -c 1 example.com
```

update the concurrent users limit to 1024
```bash
sed -i 's/^limit.*/limit = 1024/' ~/.siege/siege.conf
```
> `cat ~/.siege/siege.conf | grep limit`

for using sed command inside container
```bash
docker run --rm -it -v ${PWD}:/usr/src/app/ -w /usr/src/app/ ubuntu bash
```
