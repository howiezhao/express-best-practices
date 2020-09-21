# 路由

## 使用 `Router` 中间件组织路由

相比起使用类似 `app.get` 等方法，使用类似 `router.get` 等方法可以更好的组织代码。
如下所示：

```js
const express = require('express');
const router = express.Router();

const index = (req, res) => {
  res.send('Hello World!');
}

router.get('/', index);

module.exports = router;
```

## 路由与控制器相分离

应像上述示例一样，将路由与控制器（回调函数）相分离。
某些时候，可能会有多个回调函数处理同一个路由，
此时，分离的结构可以使代码更加清晰，可参考 [Express 官方文档](https://expressjs.com/zh-cn/guide/routing.html#route-handlers) 。

## 路由不要使用链式调用
