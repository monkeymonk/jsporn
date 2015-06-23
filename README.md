# jsporn

## Strings

#### Padding numbers
```javascript
function pad(v){
  return ('0'+v).substr(-2);
}
pad(6)  // 06
pad(13) // 13
```
> Author: Patrick Denny / Source: [Medium](https://medium.com/@p_arithmetic/a-collection-of-my-6-favorite-javascript-one-liners-7c80a4b731f8)


## Random 

#### Debugging CSS
```javascript
[].forEach.call($$("*"),function(a){
  a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)
})
```
> Author: [Addy Osmani](http://addyosmani.com/blog/) / Source: [arqex](http://arqex.com/939/learning-much-javascript-one-line-code)

## Links

- [http://wtfjs.com/](http://wtfjs.com/)
- [http://arqex.com/939/learning-much-javascript-one-line-code](http://arqex.com/939/learning-much-javascript-one-line-code)
