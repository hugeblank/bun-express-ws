# bun-express-ws
Fork of wll8's improved express-ws that utilizes Bun's built-in WebSocket implementation. For more information about what's different between wll8's version and the unscoped package please see [wll8's readme](https://github.com/wll8/express-ws#readme).


## Usage

``` sh
bun install bun-express-ws
```

``` js
const express = require(`express`)
const expressWs = require(`bun-express-ws`)
const {app, wsRoute} = expressWs(express())

app.ws(`/abc`, (ws, req) => {
  // const {params, query} = req
  ws.send(`abc`)
})
app.get(`/abc`, (req, res) => {
  res.json(`abc`)
})

app.listen(3040)
```

- For more examples see the file: [test.js](https://github.com/hugeblank/express-ws/blob/ad35c6156aed4f8d195214784ad903f22ce84536/test/index.test.ts#L15)

## License
[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2023-present, hugeblank