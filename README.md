# siege-guide

install siege
```bash
brew install siege
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

update the concurrent users limit to 500
```bash
sed -i 's/^limit.*/limit = 500/' siege.conf
```
> file location: `~/.siege/siege.conf`

for using sed command inside container
```bash
docker run --rm -it -v ${PWD}:/usr/src/app/ -w /usr/src/app/ ubuntu bash
```
