## 有限状态机

### JS 中的有限状态机（Mealy）

```js
// 每个函数是一个状态机
function state(input) {
  // 在函数中，可以自由地编写代码，处理每个状态的逻辑
  return next; // 返回值作为下一个状态
}
while (input) {
  // 获取输入
  state = state(input); // 把状态机的返回值作为下一个状态
}
```

Mealy 型的状态机，`return` 几乎是根据 `input` 在一系列逻辑语句处理后得到。

Moore 型的状态机，`return` 与 `input` 无关。



## HTTP 的协议解析

### ISO-OSI 七层网络模型

- 应用层
- 表示层
- 会话层
- 传输层
- 网络层
- 链路层
- 物理层



### 实现一个HTTP的请求

第一步

- 设计一个 HTTP 请求的类
- content-type 是一个必要的字段，要有默认值
- body 是 KV 格式
- 不同的 content-type 影响 body 的格式

第二步

- 在 Request 的构造器中收集必要的信息
- 设计一个 send 函数，把请求真实发送到服务器
- send 函数应该是异步的，所以返回 Promise

第三步 发送请求

- 设计支持已有的 connection 或者自己新建 connection
- 收到数据传给 parser
- 根据 parser 的状态 resolve Promise

第四步 ResponseParser 总结

- Response 必须分段构造，所以我们要用一个 ResponseParser 来“装配”
- ResponseParser 分段处理 ResponseText，我们用状态机来分析文本的结构

第五步 BodyParser 总结

- Response 的 body 可能根据 Content-Type 有不同的结构，因此我们会采用子 Parser 的结构来解决问题
- 以 TtrunkedBodyParser 为例，我们同样用状态机来处理 body 的格式
