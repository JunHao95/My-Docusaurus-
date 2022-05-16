---
title: Live Coding Example Page
Description: How to implement live coding in Docusaurus 
---


## Live Coding with Reach in Docusaurus

Some explanation


```jsx live
function ExampleLive(props) {
    const [count,setCount] = useState(10);

    return (
    <div>
    Hi there, you can do simple math operation using the buttons here
        <h1>{count}</h1>
        <button onClick={() => setCount(count + 1)}>Add up</button>
        <button onClick={() => setCount(count - 1)}>Subtract</button>
        <button onClick={() => setCount(0)}>Reset</button>
    </div>
    );
}
```

```jsx live
function Clock(props) {
  const [date, setDate] = useState(new Date());
  useEffect(() => {
    var timerID = setInterval(() => tick(), 1000);

    return function cleanup() {
      clearInterval(timerID);
    };
  });

  function tick() {
    setDate(new Date());
  }

  return (
    <div>
      <h2>The time now is : {date.toLocaleTimeString()} UTC+8.</h2>
    </div>
  );
}
```