###### 1. Output sẽ là gì?

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```

- [ ] A: `0 1 2` and `0 1 2`
- [ ] B: `0 1 2` and `3 3 3`
- [ ] C: `3 3 3` and `0 1 2`


###### 2. Output sẽ là gì?

```javascript
const shape = {
  radius: 10,
  diameter() {
    return this.radius * 2;
  },
  perimeter: () => 2 * Math.PI * this.radius
};

shape.diameter();
shape.perimeter();
```

- [ ] A: `20` and `62.83185307179586`
- [ ] B: `20` and `NaN`
- [ ] C: `20` and `63`
- [ ] D: `NaN` and `63`

###### 3. Output là gì?

```javascript
let c = { greeting: "Hey!" };
let d;

d = c;
c.greeting = "Hello";
console.log(d.greeting);
```

- [ ] A: `Hello`
- [ ] B: `Hey`
- [ ] C: `undefined`
- [ ] D: `ReferenceError`
- [ ] E: `TypeError`

###### 4. Output là gì?

```javascript
class Chameleon {
  static colorChange(newColor) {
    this.newColor = newColor;
    return this.newColor;
  }

  constructor({ newColor = "green" } = {}) {
    this.newColor = newColor;
  }
}

const freddie = new Chameleon({ newColor: "purple" });
freddie.colorChange("orange");
```

- [ ] A: `orange`
- [ ] B: `purple`
- [ ] C: `green`
- [ ] D: `TypeError`


###### 5. Điều gì sẽ xảy ra khi chúng ta làm thế này?

```javascript
function bark() {
  console.log("Woof!");
}

bark.animal = "dog";
```

- [ ] A: Hoàn toàn không có vấn đề gì!
- [ ] B: `SyntaxError`. Bạn không thể thêm thuộc tính theo cách này.
- [ ] C: `undefined`
- [ ] D: `ReferenceError`

###### 6. 3 giai đoạn của event propagation là gì?

- [ ] A: Target > Capturing > Bubbling
- [ ] B: Bubbling > Target > Capturing
- [ ] C: Target > Bubbling > Capturing
- [ ] D: Capturing > Target > Bubbling

###### 7. Output là gì?

```javascript
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);
```

- [ ] A: `1` `1` `2`
- [ ] B: `1` `2` `2`
- [ ] C: `0` `2` `2`
- [ ] D: `0` `1` `2`

###### 8. Output là gì?

```javascript
function checkAge(data) {
  if (data === { age: 18 }) {
    console.log("You are an adult!");
  } else if (data == { age: 18 }) {
    console.log("You are still an adult.");
  } else {
    console.log(`Hmm.. You don't have an age I guess`);
  }
}

checkAge({ age: 18 });
```


- [ ] A: `You are an adult!`
- [ ] B: `You are still an adult.`
- [ ] C: `Hmm.. You don't have an age I guess`

###### 9. Output là gì?

```javascript
var num = 8;
var num = 10;

console.log(num);
```

- [ ] A: `8`
- [ ] B: `10`
- [ ] C: `SyntaxError`
- [ ] D: `ReferenceError`

###### 10. Output là gì?

```javascript
const obj = { a: "one", b: "two", a: "three" };
console.log(obj);
```

- [ ] A: `{ a: "one", b: "two" }`
- [ ] B: `{ b: "two", a: "three" }`
- [ ] C: `{ a: "three", b: "two" }`
- [ ] D: `SyntaxError`

###### 11. Output là gì?

```javascript
for (let i = 1; i < 5; i++) {
  if (i === 3) continue;
  console.log(i);
}
```

- [ ] A: `1` `2`
- [ ] B: `1` `2` `3`
- [ ] C: `1` `2` `4`
- [ ] D: `1` `3` `4`

###### 12. Output là gì?

```javascript
const a = {};
const b = { key: "b" };
const c = { key: "c" };

a[b] = 123;
a[c] = 456;

console.log(a[b]);
```

- A: `123`
- B: `456`
- C: `undefined`
- D: `ReferenceError`

###### 13. Output là gì?

```javascript
const foo = () => console.log("First");
const bar = () => setTimeout(() => console.log("Second"));
const baz = () => console.log("Third");

bar();
foo();
baz();
```

- [ ] A: `First` `Second` `Third`
- [ ] B: `First` `Third` `Second`
- [ ] C: `Second` `First` `Third`
- [ ] D: `Second` `Third` `First`

###### 14. Output là gì?

```javascript
const person = { name: "Lydia" };

function sayHi(age) {
  console.log(`${this.name} is ${age}`);
}

sayHi.call(person, 21);
sayHi.bind(person, 21);
```

- [ ] A: `undefined is 21` `Lydia is 21`
- [ ] B: `function` `function`
- [ ] C: `Lydia is 21` `Lydia is 21`
- [ ] D: `Lydia is 21` `function`


###### 15. Output là gì?

```javascript
function sayHi() {
  return (() => 0)();
}

typeof sayHi();
```

- [ ] A: `"object"`
- [ ] B: `"number"`
- [ ] C: `"function"`
- [ ] D: `"undefined"`

###### 40. Output là gì?

```javascript
[[0, 1], [2, 3]].reduce(
  (acc, cur) => {
    return acc.concat(cur);
  },
  [1, 2]
);
```

- [ ] A: `[0, 1, 2, 3, 1, 2]`
- [ ] B: `[6, 1, 2]`
- [ ] C: `[1, 2, 0, 1, 2, 3]`
- [ ] D: `[1, 2, 6]`

###### 16. Output là gì?

```javascript
[1, 2, 3].map(num => {
  if (typeof num === "number") return;
  return num * 2;
});
```

- [ ] A: `[]`
- [ ] B: `[null, null, null]`
- [ ] C: `[undefined, undefined, undefined]`
- [ ] D: `[ 3 x empty ]

###### 17. Output là gì?

```javascript
const set = new Set([1, 1, 2, 3, 4]);

console.log(set);
```

- [ ] A: `[1, 1, 2, 3, 4]`
- [ ] B: `[1, 2, 3, 4]`
- [ ] C: `{1, 1, 2, 3, 4}`
- [ ] D: `{1, 2, 3, 4}`

###### 18. Output là gì?

```javascript
const numbers = [1, 2, 3, 4, 5];
const [y] = numbers;

console.log(y);
```

- [ ] A: `[[1, 2, 3, 4, 5]]`
- [ ] B: `[1, 2, 3, 4, 5]`
- [ ] C: `1`
- [ ] D: `[1]`


###### 19. Output là gì?

```javascript
const value = { number: 10 };

const multiply = (x = { ...value }) => {
  console.log((x.number *= 2));
};

multiply();
multiply();
multiply(value);
multiply(value);
```

- [ ] A: `20`, `40`, `80`, `160`
- [ ] B: `20`, `40`, `20`, `40`
- [ ] C: `20`, `20`, `20`, `40`
- [ ] D: `NaN`, `NaN`, `20`, `40`


###### 20. Output là gì?

```javascript
let newList = [1, 2, 3].push(4)

console.log(newList.push(5))
```

- [ ] A: `[1, 2, 3, 4, 5]`
- [ ] B: `[1, 2, 3, 5]`
- [ ] C: `[1, 2, 3, 4]`
- [ ] D: `Error`

###### 21. Output là gì?

```javascript

const output = `${[] && 'Im'}possible!
You should${'' && `n't`} see a therapist after so much JavaScript lol`
```

- [ ] A: `possible! You should see a therapist after so much JavaScript lol`
- [ ] B: `Impossible! You should see a therapist after so much JavaScript lol`
- [ ] C: `possible! You shouldn't see a therapist after so much JavaScript lol`
- [ ] D: `Impossible! You shouldn't see a therapist after so much JavaScript lol`

###### 22. Output là gì?

```javascript
const one = (false || {} || null)
const two = (null || false || "")
const three = ([] || 0 || true)

console.log(one, two, three)
```

- A: `false` `null` `[]`
- B: `null` `""` `true`
- C: `{}` `""` `[]`
- D: `null` `null` `true`


###### 23. Phép toán nào sau đây làm thay đổi mảng gốc?

```javascript
const emojis = ['✨', '🥑', '😍']

emojis.map(x => x + '✨')
emojis.filter(x => x !== '🥑')
emojis.find(x => x !== '🥑')
emojis.reduce((acc, cur) => acc + '✨')
emojis.slice(1, 2, '✨')
emojis.splice(1, 2, '✨')
```

- [ ] A: `All of them`
- [ ] B: `map` `reduce` `slice` `splice`
- [ ] C: `map` `slice` `splice`
- [ ] D: `splice`


###### 24. Phép toán này dùng để làm gì?

```javascript
JSON.parse()
```

- [ ] A: Parse JSON thành một giá trị JavaScript
- [ ] B: Parse một JavaScript object thành JSON
- [ ] C: Parse giá trị JavaScript bất kì thành JSON
- [ ] D: Parse JSON thành một JavaScript object

###### 25. Ouput là gì?

```javascript
const myPromise = Promise.resolve("Woah some cool data");

(async () => {
	try {
		console.log(await myPromise);
	} catch {
		throw new Error(`Oops didn't work`);
	} finally {
		console.log("Oh finally!");
	}
})();
```

- [ ] A: `Woah some cool data`
- [ ] B: `Oh finally!`
- [ ] C: `Woah some cool data` `Oh finally!`
- [ ] D: `Oops didn't work` `Oh finally!`

###### 26. Làm thế nào có thể gọi hàm `sum` trong `index.js` từ `sum.js?`

```javascript
// sum.js
export default function sum(x) {
	return x + x;
}

// index.js
import * as sum from "./sum";
```

- [ ] A: `sum(4)`
- [ ] B: `sum.sum(4)`
- [ ] C: `sum.default(4)`
- [ ] D: Default aren't imported with `*`, only named exports

