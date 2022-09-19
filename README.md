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

## Week 2 Exercises

1. Palindrome strings

```js
const isPalindrome = (str) => {
	let w1 = str.toString().toLowerCase()
  let w2 = str.toString().toLowerCase().split("").reverse().join("")
  return w1 === w2
}
```

2. Well of Ideas - Easy Version

```js
function well(x){
  let ideasCounter = x.filter(idea => idea=='good').length
  if(ideasCounter == 1 || ideasCounter == 2){
    return 'Publish!'
  } else if (ideasCounter >= 2){
    return 'I smell a series!'
  }
    return 'Fail!'
}
```

3. Managing Events in React JS

```js
class TodoApp extends React.Component {
  constructor(props) {
    super(props)
    this.state = {
    	value: 0
    }
  }
  
  render() {
    return (
      <div>
        <label id="counter">{`Value is ${this.state.value}`}</label>
        <button id="decrement" onClick={()=>{this.setState({value: this.state.value - 1})}}>-</button>
        <button id="increment" onClick={()=>{this.setState({value: this.state.value + 1})}}>+</button>
      </div>
    )
  }
}

ReactDOM.render(<TodoApp />, document.querySelector("#app"))
```

4. Santa wish list form in ReactJS

```js
class TodoApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
    	name: '',
      wish: '',
      priority: "1",
    };
    
    const send = props

    this.handleChangeName = this.handleChangeName.bind(this);
    this.handleChangeWish = this.handleChangeWish.bind(this);
    this.handleChangePriority = this.handleChangePriority.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  

  handleChangeName(event) {
    this.setState({name: event.target.value});
  }
  
  handleChangeWish(event) {
    this.setState({wish: event.target.value});
  }
  
  handleChangePriority(event) {
    this.setState({priority: event.target.value});
  }

  handleSubmit(event) {
  	console.log(this.state)
    props.send(this.state)
    event.preventDefault();
  }
  
  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input id="name" type="text" value={this.state.name} onChange={this.handleChangeName} />
        </label>
        <label>
          Wish:
          <textarea id="wish" value={this.state.wish} onChange={this.handleChangeWish} />
        </label>
        <label>
          Priority
          <select id="priority" value={this.state.priority} onChange={this.handleChangePriority}>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
          </select>
        </label>
        <input type="submit" value="Submit" />
      </form>
    )
  }
}

ReactDOM.render(<TodoApp />, document.querySelector("#app"))
```
