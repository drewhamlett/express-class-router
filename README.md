# Express Class Router


### Example
```js

//home.js
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

```js
//routes.js
const router = new Router('./server/controllers')
router.get('/', 'home#index')

export default {
  router
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

