# deno-demo
```
Deno run index.ts
-> Hello Deno
```
```
Deno run index.ts
->Uncaught PermissionDenied: network access to "http://hn.algolia.com/api/v1/search?query=javascript", run again with the --allow-net flag
```
在 Deno 的域中操作，可以无需授予Deno任何许可而做很多事情而。但是如果我们想超越 Deno 的职责范围，则需要明确允许它。在这种从远程 API 获取数据的情况下，需要允许网络请求
```
Deno run --allow-net index.ts
```
再次运行 Deno 程序后，你应该在命令行上看到一系列 Hacker News 文章。
