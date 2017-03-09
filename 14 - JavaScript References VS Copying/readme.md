# JavaScript References VS Copying

## call by "value" or call by "reference
Javascript is always pass by value, but when a variable refers to an object (including arrays), the "value" is a reference to the object.

只要記住一個原則: 無論是數值、字串、物件、陣列、布林，JavaScript函式參數一律傳值(call by value)，但為物件、陣列時這個value對物件而言就是reference

## 所以我們可以記成
* String、Number、Boolean => call by value
* Object、Array、Function => call by reference

## call by vlaue
* Number、String、Boolean

Number
```js
let age = 100;
let age2 = age;
console.log(age, age2) // 100,100
age = 200;
console.log(age, age2) // 200,100
```
String
```js
let name = 'peggy';
let name2 = name;
console.log(name, name2) // peggy,peggy
name = 'wooooo';
console.log(name, name2) // wooooo,peggy
```
Boolean
```js
let a = true;
let b = a;
console.log(a,b) // true,true
a = false;
console.log(a,b) // false,true
```
## call by reference
* Array、Object、Function

Array
```js
const players = ['Wes', 'Poppy'];
const team = players;
console.log(players,team) // ["Wes", "Poppy"] ["Wes", "Poppy"]
team[1] = 'woooo';
console.log(players,team) // ["Wes", "woooo"] ["Wes", "woooo"]
```
### 解決call by reference
* xxx.slice()
* [].concat(xxx)
* [...xxx]
* Array.from(xxx)
```js
const team2 = players.slice();
const team3 = [].concat(players);
const team4 = [...players];
const team5 = Array.from(players);
console.log(players,team2) // ["Wes", "Peggy"] ["Wes", "Peggy"]
team[1] = 'woooo';
console.log(players,team2) // ["Wes", "woooo"] ["Wes", "Peggy"]
```
Object
```js
const person = {
    name:'peggy',
    age:22
}
const p2 = person;
console.log(p2.name,person.name) // peggy peggy
person.name = 'bebo';
console.log(p2.name,person.name) // bebo bebo
```
### 解決call by reference
* Object.assign({}, xxx , {"想修改的name:value"})
* {...xxx} ES6尚未支援
* 以上只能用到1層 nested的無效 會reference
    * JSON.parse(JSON.stringify(xxx))
```js
const person = {
    name:'peggy',
    age:22
}
const p2 = Object.assign({},person,{number:100,age:100})
console.log(p2) // Object {name: "peggy", age: 100, number: 100}
```
* 巢狀
```js
const pg = {
    name:'peggy',
    age:22,
    hi:{
        name:'bebo'
    }
}
const pggg = Object.assign({},pg)
pggg.hi.name = 'nooo'
console.log(pg.hi,pggg.hi)    // nooo nooo
```
```js
const pggg2 = JSON.parse(JSON.stringify(pg)) // 不可與前面同時進行，pg會被修改
console.log(pg.hi,pggg2.hi)  // bebo nooo 
```