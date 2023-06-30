## For Harbor Dockerfile

```
docker login {IP}:80 -u Ishan -p {PASSWORD}
```

```
docker build -t ishanjainn/test .
```

```
docker tag ishanjainn/test {IP}:80/test/ishan:1.0.0
```

```
docker push {IP}:80/test/ishan:1.0.0
```

```
docker pull {IP}:80/test/ishan
```

## For Harbor Chart
