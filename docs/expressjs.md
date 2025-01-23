# expressjs

- `$ npm install express --save`

## App

```jsx
const express = require('express')
const app = express()

app.get('/user/:id', function (request, respond) {
  respond.setHeader('Content-Disposition', 'attachment; filename="test.txt"')
  respond.send(`
  <div>
    id: user ${request.params.id} <hr/>
    hostname: ${request.hostname} <hr/>
    protocol: ${request.protocol} <hr/> <br/> <br/> <br/>

    Accept: ${request.headers['accept']} <hr/>
    Accept-Encoding: ${request.headers['accept-encoding']} <hr/>
    Accept-Language: ${request.headers['accept-language']} <hr/>
    Cache-Control: ${request.headers['cache-control']} <hr/>
    Connection: ${request.headers['connection']} <hr/>
    Host: ${request.headers['host']} <hr/>
    If-None-Match: ${request.headers['if-none-match']} <hr/>
    sec-ch-ua: ${request.headers['sec-ch-ua']} <hr/>
  </div>
  `)
})

app.get('/download', function (request, respond) {
  respond.send(`
  <div>
    id: user ${request.params.id} <hr />
    hostname: ${request.hostname} \n
    protocol: ${request.protocol} \n

    Accept: ${request.headers.accept}
  </div>
  `)
})

app.listen(3000)
```

- `npm i multer`

```jsx
const express = require('express')

const app = express()
const port = 3000

app.use(express.static('public'))

app.get('/', function (req, res) {
  res.send('Hello World')
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```

[Express - Node.js web application framework](https://expressjs.com/)

[Express JS Crash Course](https://www.youtube.com/watch?v=L72fhGm1tfE&t=273s)

```jsx
const path = require('path')
const express = require('express')
const logger = require('./middleware/logger')
const members = require('./members.js')

const app = express()

// Set static folder
app.use(express.static(path.join(__dirname, 'public')))

app.use(logger)

app.get('/api/members', (req, res) => res.json(members))

app.get('/', function (req, res) {
  // res.sendFile(path.join(__dirname, 'public', 'index.html'))
  // res.send('<h1>Hello Express</h1>')
})

const PORT = process.env.PORT || 5000

app.listen(PORT, () => console.log(`Server started on port ${PORT}`))

// 中间件方法, 可以访问request和response的方法
```

```jsx
const express = require('express')
const router = express.Router()

// localhost:5000/api/members
router.get('/', (req, res, next) => {

})

// localhost:5000/api/members/6
router.get('/:id', (req, res, next) => {
  const id = req.params.id
})

router.post('/', (req, res) => {
  res.send(req.body)
})

module.exports = router
```

