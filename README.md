# core-code-upskilling-readme

## Week 1 Exercises

1. Ensure question

```js
const ensureQuestion = (word) => {
	if(word.slice(-1) !== '?'){
  	return word += '?'
  }
  return word
}
```

2. Reversed Words

```js
const reversedWords = (word) => {
	let wordsArray = word.split(" ")
  return wordsArray.reverse().join(" ")
}
```

3. Smallest int

```js
const smallestInt = (intArray) => {
  return intArray.sort((a,b) => a-b)[0]
}
```

4. Odd or Even

```js
const oddOrEven = (intArray) => {
  let total =intArray.reduce((sum, val) => sum + val, 0)
  return total % 2 === 0 ? 'even' : 'odd'
}
```
