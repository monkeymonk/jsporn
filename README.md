# jsporn

## Strings


#### Making text L337

```javascript
function L337(str) { 
  return str.replace(/[a-z]/g, function f(a) {
    return "4BCD3F6H1JKLMN0PQR57"[parseInt(a, 36) - 10] || a.replace(/[a-t]/gi, f);
  }); 
}
```

> Author: [Markandey Singh](https://twitter.com/markandey) / Source: [JSOneLiners](http://www.jsoneliners.com/category/function/)


#### Padding numbers

```javascript
function pad(num, length) {
  return (Array(length).join('0') + num).slice(-length);
}

pad(6, 2)  // 06
pad(13, 10) // 0000000013
```

***

## Conversion

#### ParseInt

```javascript
console.log(["10", "10", "10"].map(parseInt));
// return [10, NaN, 2]
```


***

## Random 


#### Incrementing stuff with nested loops

Because why not ?

```javascript 
for (var i = 0, j = 0; i < 10 && j < 10; j++, i = (j == 10) ? i + 1 : i, j = (j == 10) ? j = 0 : j, console.log(i, j)) {}
```

> Author: [Nicholas Ortenzio](https://twitter.com/p_arithmetic) / Source: [Medium](https://medium.com/@p_arithmetic/a-collection-of-my-6-favorite-javascript-one-liners-7c80a4b731f8)


#### Getting URL parameters

```javascript
function getQueryParams() {
  return document.location.search.replace(/(^\?)/, '').split('&').reduce(function (o, n) {
    n = n.split('='); o[n[0]] = n[1]; return o;
  }, {});
}

getQueryParams()  // {key: "value"}
```

> Author: [Nicholas Ortenzio](https://twitter.com/p_arithmetic) / Source: [Medium](https://medium.com/@p_arithmetic/a-collection-of-my-6-favorite-javascript-one-liners-7c80a4b731f8)


#### Debugging CSS

```javascript
[].forEach.call($$("*"), function (a) {
  a.style.outline = "1px solid #" + (~~(Math.random() * (1 << 24))).toString(16);
});
```

> Author: [Addy Osmani](http://addyosmani.com/blog/) / Source: [arqex](http://arqex.com/939/learning-much-javascript-one-line-code)


### Array concat unique

```javascript
var newArray = [].concat(a, b.filter(function (item) {
    return a.indexOf(item) < 0;
}));
```

### Array randow

```javascript
[1, 2, 3, 4, 5].sort(function () { return Math.random() - 0.5; });
```


### Array find smallest/largest

```javascript
var larget = Math.max.apply(Math, [0, 5, 19, 7, -1]); // 19

var smallest = Math.min.apply(Math, [0, 5, 19, 7, -1]); // -1
```


### Array create + populate

```javascript
Array.apply(null, {length: 10}).map(Number.call, Number); // [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```


### Object `indexOf`

```javascript
var index = [{id: 3}].map(function (e) { return e.id; }).indexOf();
```


### URI Parser

```javascript
var parser = document.createElement('a');
parser.href = "http://example.com:3000/pathname/?search=test#hash";

parser.protocol; // => "http:"
parser.hostname; // => "example.com"
parser.port;     // => "3000"
parser.pathname; // => "/pathname/"
parser.search;   // => "?search=test"
parser.hash;     // => "#hash"
parser.host;     // => "example.com:3000"
```


### "Y-m-d H:m:s" to JS Date

```javascript
function convertDate(time) {
    var CustomDate = Function.prototype.bind.apply(Date, [null].concat(time.split(/[\s:-]/)).map(function (v, i) {
      return (i === 2 ? --v : v); 
    }));
    return new CustomDate();
}
```



## Links

- [http://wtfjs.com/](http://wtfjs.com/)
- [http://arqex.com/939/learning-much-javascript-one-line-code](http://arqex.com/939/learning-much-javascript-one-line-code)


## Todo

- [ ] Sort those things a little bit
