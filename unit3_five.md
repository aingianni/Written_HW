# Mini-Max Sum

## Explanation
First i run a sort becuase if all the numbers are in order I can just take one index off the array to get the desired amount of numbers for the min. We run the loop and add the numbers to the counter for the min Sum. Then we reverse the array and run a another loop again cutting off the last number adding each number to the counter to get the max number. Per the challenge we console log the two values with a space in the middle.

```
function miniMaxSum(arr) {
    let min = 0;
    let max = 0;
    
    arr.sort((a,b) => a-b)
    
    for (let i=0; i < arr.length-1; i++) {
        min += arr[i];
    }
    arr.reverse();
    for (let i=0; i < arr.length-1; i++) {
        max += arr[i];
    }
    
    console.log(min + ' ' + max)
}
```

## Screenshot
<img src="https://i.imgur.com/dF5tAZv.png">