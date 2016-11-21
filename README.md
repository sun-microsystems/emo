# Emo

Emo is a dynamic language, emojii based (and a subset of JavaScript)☠️

> WIP :construction:

## Predefined methods

```
 🖥("hello 🌍") // display hello 🌍
 📅(12/12/68, 🇫🇷).getMonthName() == "december"
 🚧 { doSomeThing() } 💣 { ifError() } 🍻 { ifSuccess() }
 
```

## No class, only emojii types

```
let buster = 🐰 {
  name: "Buster",
  eat: (🍏 something) { // you can set the expected type of the argument
    // foo
  }
}

let kungFuPanda = 🐼 {
  name: "Po",
  sayHello: () => {
    🖥(this.name) // display "Po"
  }
}

```

### No inheritance but... each type has an interface

- `🐼 is animal == true` 
- `🐹 is animal == true` 
- `🍄 is mushroom == true` 
- `🍊 is fruit == true` 
- `🍋 is fruit == true` 
- `🍆 is vegetable == true` 

## Functional types

Emotion has 3 functional types:

 - 💊 Monade
 - ❓ `Maybe`, ☠️ `None`, ✨ `Some`
 - ⁉️ `Result`, ❌ `Error`, ✅ `Ok`
 
 ### Functor/Monad
 
 ```
let counter = 💊(0)
let add = (n)-> n+1
counter.map(add).map(add) == 💊(2)
 ```
 
 ### Maybe
 
 ```
 ❓(null) == ☠️
 ❓(42) == ✨[42]
 ❓(null).getOrElse(42) == 42
 ```
 
 ### Either
 
 ```
 ⁉️(42) == ✅[42]
 ⁉️(new Error("Houston?")) == ❌["Houston?"]
 ```




