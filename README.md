# express-rate-limit-sample
you can use [express-rate-limit](https://www.npmjs.com/package/express-rate-limit) sample.

# install
you can use yarn or npm command.
* yarn install
* npm insatll

# start app
* yarn start
* npm start

# check
* First access to "localhost:3000" and you can see "ExpressXXX"
* Second access(within 10seconds from first access) and you can see "Too many requests, please try again later." and get http response code as 429.

# change limit config
You can chenge config in [app.js](https://github.com/pirobeem/express-rate-limit-sample/blob/master/app.js).
```
const limiter = rateLimit({
  windowMs: 10000, // maxのリクエストを許可する最大ミリ秒
  max: 1, // windowMs以内 リクエスト最大数（maxまでリクエストはOK）
  keyGenerator: () => 'test', // デフォルトはIP単位の制限なので、固定値にしてアプリ単位にする
})
```
