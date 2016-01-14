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
function pad(v) {
  return ('0' + v).substr(-2);
}

pad(6)  // 06
pad(13) // 13
```
> Author: Patrick Denny / Source: [Medium](https://medium.com/@p_arithmetic/a-collection-of-my-6-favorite-javascript-one-liners-7c80a4b731f8)


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

## Links

- [http://wtfjs.com/](http://wtfjs.com/)
- [http://arqex.com/939/learning-much-javascript-one-line-code](http://arqex.com/939/learning-much-javascript-one-line-code)
