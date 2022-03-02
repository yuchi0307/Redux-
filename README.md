<h2>Redux使用</h2>

![下載](https://user-images.githubusercontent.com/67968321/156372576-8dcfa895-8be8-4bea-b2be-7f9f08f9cbd2.png)

<ol>
<li> npm init -y </li> 
<li> npm install redux </li> 
<li> 執行js：node 檔名 </li>
</ol>


```
const redux = require('redux');

const counterReducer = (state = { counter: 0 }, action) =>{
    return{
        counter: state.counter + 1
    };
};

const store = redux.createStore(counterReducer);

const conunterSubscriber = ()=>{
    const latestState = store.getState();
    console.log(latestState);
};

store.subscribe(conunterSubscriber);

store.dispatch({type: 'increment'});
```
