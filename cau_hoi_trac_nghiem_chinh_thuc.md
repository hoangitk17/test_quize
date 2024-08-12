###### 1. Output là gì?

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

###### 2. Output là gì?

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

###### 3. Output là gì?

```javascript
const obj = { a: "one", b: "two", a: "three" };
console.log(obj);
```

- [ ] A: `{ a: "one", b: "two" }`
- [ ] B: `{ b: "two", a: "three" }`
- [ ] C: `{ a: "three", b: "two" }`
- [ ] D: `SyntaxError`

###### 4. Output là gì?

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

###### 5. Output là gì?

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

###### 6. Output là gì?

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

###### 7. Điều gì sẽ xảy ra khi chúng ta làm thế này?

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


###### 8. Output là gì?

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

###### 9. Output là gì?

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

###### 10. Output là gì?

```javascript
const set = new Set([1, 1, 2, 3, 4]);

console.log(set);
```

- [ ] A: `[1, 1, 2, 3, 4]`
- [ ] B: `[1, 2, 3, 4]`
- [ ] C: `{1, 1, 2, 3, 4}`
- [ ] D: `{1, 2, 3, 4}`


###### 11. Output là gì?

```javascript
const numbers = [1, 2, 3, 4, 5];
const [y] = numbers;

console.log(y);
```

- [ ] A: `[[1, 2, 3, 4, 5]]`
- [ ] B: `[1, 2, 3, 4, 5]`
- [ ] C: `1`
- [ ] D: `[1]`


###### 12. Output là gì?

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

###### 13. Output là gì?

```javascript

const output = `${[] && 'Im'}possible!
You should${'' && `n't`} see a therapist after so much JavaScript lol`
```

- [ ] A: `possible! You should see a therapist after so much JavaScript lol`
- [ ] B: `Impossible! You should see a therapist after so much JavaScript lol`
- [ ] C: `possible! You shouldn't see a therapist after so much JavaScript lol`
- [ ] D: `Impossible! You shouldn't see a therapist after so much JavaScript lol`

###### 14. Output là gì?

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
- E: `{}` `null` `[]`


###### 15. Ouput là gì?

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

###### 16. Làm thế nào có thể gọi hàm `sum` trong `index.js` từ `sum.js?`

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

###### 17. Output là gì?

```javascript
let c = { greeting: "Hey!" };
let d;

d = c;
c.greeting = "Hello";
console.log(d.greeting);
```

- [ ] A: `Hello`
- [ ] B: `Hey!`
- [ ] C: `undefined`
- [ ] D: `ReferenceError`
- [ ] E: `TypeError`


###### 18. Output sẽ là gì?

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

###### 19. Output là gì ?

```javascript

(function(){
 setTimeout(()=> console.log(1),2000);
 console.log(2);
 setTimeout(()=> console.log(3),0);
 console.log(4);
})();
```

- [ ] A: `1 2 3 4`
- [ ] B: `2 3 4 1`
- [ ] C: `2 4 3 1`
- [ ] D: `4 3 2 1`

###### 20. Output sẽ là gì?

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

###### 21. Output là gì ?


```javascript
print(typeof(NaN));
```

- [ ] A: `object`
- [ ] B: `number`
- [ ] C: `string`
- [ ] D: Không đáp án nào đúng


