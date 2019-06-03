# This is ss-server docker-compose file
## Variable:
```
$UUID: for v2ray to identify from server to client
$ADDR: for v2ray client connect to server
$PASSWD: for shadowsock
```

## Step1:
Generator UUID from [UUID Generator](https://www.uuidgenerator.net/)
Change UUID in ./v2ray-server/config.json and v2ray-client-config.json

## Step2:
Change IPADDR in ./v2ray-client-config.json which is used by your vps ip address.

## Step3:
Use Homebrew to install [v2ray](https://github.com/v2ray/homebrew-v2ray)

## Step4:
Copy file from ./v2ray-client-config.json to /usr/local/etc/v2ray/config.json

## Step5:
Start your service by ```docker-compose up -d``` and start your client by ```brew services start v2ray-core```.

## Step6:
Setup your http proxy on port 8000 and socks on port 8001


### P.S.
You can find everything in [v2ray](https://github.com/v2ray/v2ray-core) and [shadowsocks](https://github.com/shadowsocks/shadowsocks-libev).
