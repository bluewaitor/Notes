# 基本类型

## Boolean 布尔

```ts
let isDone: boolean = false;
```

## Number 数值

```ts
let decimal: number = 6;
let hex: number = 0xf00d;
let binary: number = 0b1010;
let octal: number = 0o744;
```

## String 字符串

```ts
let color: string = "blue";
color = "red";

let fullName: string = `Bob Bobbington`;
let age: number = 37;
let sentence: string = `Hello, my name is ${fullName}.

I'll be ${age + 1} years old next month`;
```

## Array 数组

```ts
let list: number[] = [1, 2, 3];
let anotherList: Array<number> = [1, 2, 3];
```

## Tuple 元组

```ts
let x: [string, number];
x = ["hello", 10];
x = [10, "hello"];

console.log(x[0].substr(1));
console.log(x[1].substr(1));
```

## Enum 枚举

```ts
enum Color {Red, Green, Blue}
let c: Color = Color.Green;
```

## Any 任何


