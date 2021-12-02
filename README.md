# haproxy-spoe
Example of haproxy with spoe filters

`curl -X POST -H 'Content-Type: application/json' -d '{"jsonrpc":"2.0","method":"eth_blockNumber","id":1}' -X POST http://127.0.0.1`

```
$ go run *.go
2021/12/02 08:13:08 listen 9000
2021/12/02 08:13:10 handle request EngineID: '8b45ee6d-63f9-4fd9-a7bd-ded94b8f61d7', StreamID: '4', FrameID: '1' with 1 messages
2021/12/02 08:13:10 request body length 51
2021/12/02 08:13:10 cap-hdr-request host: 127.0.0.1
2021/12/02 08:13:10 cap-hdr-request user-agent: curl/7.68.0
2021/12/02 08:13:10 cap-hdr-request accept: */*
2021/12/02 08:13:10 cap-hdr-request content-type: application/json
2021/12/02 08:13:10 cap-hdr-request content-length: 51
2021/12/02 08:13:10 handle request EngineID: '8b45ee6d-63f9-4fd9-a7bd-ded94b8f61d7', StreamID: '4', FrameID: '2' with 1 messages
2021/12/02 08:13:10 response body length 45
2021/12/02 08:13:10 body: {"jsonrpc":"2.0","id":1,"result":"0xc85e87"}

2021/12/02 08:13:10 cap-hdr-response content-type: application/json
2021/12/02 08:13:10 cap-hdr-response date: Thu, 02 Dec 2021 13:13:10 GMT
2021/12/02 08:13:10 cap-hdr-response content-length: 45
2021/12/02 08:13:10 trace-context: abc-123
```
