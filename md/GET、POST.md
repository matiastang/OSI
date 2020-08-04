# GET、POST

## GET

## POST

## GET、POST区别

1）传送方式：get 通过地址栏传输，post 通过报文传输
2）传送长度：get 参数有长度限制（受限于 url 长度），而 post 无限制
3）GET 产生一个 TCP 数据包（对于 GET 方式的请求，浏览器会把 http header 和 data 一并发送出去，服务器响应 200 返回数据），POST 产生两个 TCP 数据包（对于 POST，浏览器先发送 header，服务器响应 100 continue，浏览器再发送 data，服务器响应 200 ok 返回数据）
4）get 请求参数会被完整保留在浏览历史记录里，而 post 中的参数不会被保留
5）在做数据查询时，建议用 GET 方式；而在做数据添加、修改或删除时，建议用 post 方式