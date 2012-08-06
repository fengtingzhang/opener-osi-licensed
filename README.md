# It Opens Stuff

That is, in your desktop environment. This will make *actual windows pop up*, with stuff in them:

```bash
npm install opener -g

opener http://google.com
opener ./my-file.txt
opener firefox
opener npm run lint
```

Also if you want to use it programmatically you can do that too:

```js
var opener = require("opener");

opener("http://google.com");
opener("./my-file.txt");
opener("firefox");
opener("npm run lint");
```

## Use It for Good

Like opening the user's browser with a test harness in your package's test script:

```json
{
    "scripts": {
        "test": "opener ./test/runner.html"
    },
    "devDependencies": {
        "opener": "*"
    }
}
```

## Why

Because Windows has `start`, Macs have `open`, and *nix has `xdg-open`. At least
[according to some guy on StackOverflow](http://stackoverflow.com/q/1480971/3191). And I like things that work on all
three. Like Node.js. And Opener.
