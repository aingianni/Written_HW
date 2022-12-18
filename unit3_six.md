# Time Conversion

## Explanation
The first thing we need to check is whether it is AM or PM, which means we need to check if index 8 is an 'A' or a 'P'. If it is 'AM' we need to check if it is '12 AM' because it is the '12' needs to be swapped for '00' for military time. We return the '00' followed by the unchanged substring going from index 2-8. If it doesnt equal '12' we just return the string from index 0-8.

For 'PM' we need to do similar thing and check for the '12' because '12 PM' is the only 'PM' that doesnt require us to change the '12'. For everything else we need to take that first number and add it to our 12 hour clock to get the military time above 12. We store these in variables to make the return statement easier to write out.

```
function timeConversion(s) {
    if (s[8] === 'A') {
        if (s[0] === '1' && s[1] === '2') {
            return '00' + s.substring(2, 8);
        }
        return s.slice(0,8);
    } else if (s[8] === 'P') {
        if (s[0] === '1' && s[1] === '2') {
            return '12' + s.substring(2, 8);
        }
        const firstNum = s.substring(0, 2);
        const newNum = parseInt(firstNum) + 12;
        return newNum.toString() + s.substring(2, 8);
    }
}
```

For kicks and giggles here is my original submission for this problem near the beginning of the course.

```
function timeConversion(s) {
    const newArr = Array.from(s);
    let firstDigit = parseInt(newArr[0]);
    let secondDigit = parseInt(newArr[1]);
    
    if (firstDigit === 1 && secondDigit === 2 && newArr[8] === "A") {
      firstDigit = 0;
      secondDigit = 0;
      newArr.splice(0, 1, firstDigit.toString());
      newArr.splice(1, 1, secondDigit.toString());
      newArr.pop();
      newArr.pop();
      return newArr.join('');
    }
  
    if (newArr[8] === "P") {
      if (firstDigit === 1 && secondDigit === 2) {
        newArr.pop();
        newArr.pop();
        return newArr.join('');
      } 
      firstDigit += 1;
      secondDigit += 2;
      newArr.splice(0, 1, firstDigit.toString());
      newArr.splice(1, 1, secondDigit.toString());
      newArr.pop();
      newArr.pop();
      return newArr.join('');      
    } else {
      newArr.pop();
      newArr.pop();
      return newArr.join('');
    }
}
```

## Screenshot
<img src="https://i.imgur.com/pbAQEbW.png">