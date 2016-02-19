
```html
<script src="rx.js"></script>
```

Or if we're using [Node.js](http://node.js), we can reference it as such:

```js
var Rx = require('rx');
```

```js
var source = Rx.Observable.create(function (observer) {
  // Yield a single value and complete
  observer.onNext(42);
  observer.onCompleted();

  // Any cleanup logic might go here
  return function () {
    console.log('disposed');
  }
});

var subscription = source.subscribe(
  function (x) { console.log('onNext: %s', x); },
  function (e) { console.log('onError: %s', e); },
  function () { console.log('onCompleted'); });

// => onNext: 42
// => onCompleted

subscription.dispose();
// => disposed
```

