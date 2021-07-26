This is the demo that shows a datasheet.

<img src="https://images2018.cnblogs.com/blog/359743/201806/359743-20180619222509796-2072292283.png" />

## Table of Contents

- [Reference](#reference)
- [Fetch](#fetch)
- [Run](#run)

## Fetch
```js
  const fetchPosts = subreddit => dispatch => {
    dispatch(requestPosts(subreddit))
    return fetch(`http://localhost:8080/${subreddit}`)
      .then(response => response.json())
      .then(json => dispatch(receivePosts(subreddit, json)));
}
```

### Data
    One row of data is as follows:
```json
{
  "userId":8,
  "userName":"test8",
  "name":"test",
  "passwrod":"$2a$04$HcffZJMrgN0.lmEFpC4KTeeQhitLYzrH0uTCpGRJRBw4o03ms.qWa",
  "email":"test4@163.com",
  "address":"wuhan-hanyang"
}
```

## Run

```bash
npm install --save react
npm install --save react-dom
npm install --save react-scripts
npm install --save redux
npm install --save react-redux
npm install --save redux-logger
npm install --save redux-thunk
npm start
```

### typescript
> The new version of redux requires typescript.
```bash
npm install --save typescript
```


## Reference
* [async(redux-thunk)](https://github.com/reduxjs/redux/tree/master/examples/async)
* [demo-jpa](https://github.com/xiaobin80/demo-jpa-spring-boot2-mysql)