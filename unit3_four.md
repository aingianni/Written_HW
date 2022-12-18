# Plus/Minus HackerRank Problem

## Explanation
We are running a simple for loop that is tracking all positive/negative numbers and all zeros. Then we return those trackers divided by the length of the array and rounded off to the 6th decimal point.

```
function plusMinus(arr) {
    let posNum = 0;
    let negNum = 0;
    let zero = 0;
    let n = arr.length;

    for (let i = 0; i < arr.length; i++) {
        if (arr[i] > 0) {
            posNum++;
        } else if (arr[i] === 0) {
            zero++;
        } else if (arr[i] < 0) {
            negNum++;
        }
    }
    
    posNum /= n;
    negNum /= n;
    zero /= n;
    
    console.log(posNum.toFixed(6));
    console.log(negNum.toFixed(6));
    console.log(zero.toFixed(6));
}
```

## Screenshot
<img src="https://i.imgur.com/EK8SwcB.png">