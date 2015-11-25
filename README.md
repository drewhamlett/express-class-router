# Express Class Router


### Example
```js

function log(req, res, next) {
  console.log('hello')
  next()
}

export default class Home {

  beforeAction = [log]

  index(req, res) {
    res.render('home')
  }
}
```


### Example with objection.js
```js

export default class Posts {

  async index(req, res) {
    const posts = await Post.query().limit(10)
    return res.json(posts)
  }
}
```

