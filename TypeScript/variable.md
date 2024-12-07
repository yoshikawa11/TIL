* 変数宣言は`const`、`let`
  * 再代入するのなら`let`を、そうでないなら`const`を利用する

```ts
// constは再代入不可
const name = "小動物";
name = "哺乳類";  // Cannot assign to 'name1' because it is a constant.(2588)

// 変更がある変数はlet
// 三項演算子を使えばconstにもできる
const mode = "slack";
let name2;
if (mode === "slack") {
    name2 = "小型犬";
} else if (mode === "twitter") {
    name2 = "小動物";
}
console.log(name2);

const name3 = mode === "slack" ? "小型犬" : "小動物";
console.log(name3);
```

* `const`はあくまで再代入を禁止するもので、オブジェクトの要素の変更はできる。
  * 読み取り専用にするには `readonly` プロパティを設定する

```ts
const obj = { a: 1 };
// obj = { a: 2 }; 　Cannot assign to 'obj' because it is a constant.
obj.a = 2;
console.log(obj.a);
console.log(obj); // { "a": 2 }

// obj.b = 1;  Property 'b' does not exist on type '{ a: number; }'.
// obj = {a : 4}; Cannot assign to 'obj' because it is a constant.
```
