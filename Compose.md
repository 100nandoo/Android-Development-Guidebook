# Compose
Built-in composables are designed for unidirectional data flow

## Layout
* Row
* Column
* Box
* Constraint Layout

## Customization
Use slot API to provide customization

## Material Design
* Scafford Provide basic material design for basic UI component

## Modifier
* You can chain multiple modifier
* There is 2 "types" of modifier
    - Modifier
    - Layout modifier

## State
Best Practice:
* Make your composable stateless, by doing so it provide some benefit
    - Easier testing
    - Encourage reusable

## UI Update Loop
[Graph](https://developer.android.com/codelabs/jetpack-compose-state/img/1be37cbec4304401.png)
* Event
* Update State
* Display State

## Memory
Each composable can have built in memory by using `remember`
```kotlin
val state = remember { mutableStateOf(default) }
var value by remember { mutableStateOf(default) }
val (value, setValue) = remember { mutableStateOf(default) }
```