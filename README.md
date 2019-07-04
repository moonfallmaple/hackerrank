# hackerrank

Question1 ：Get the number of max match
```
Sample Input
9
10 20 20 10 10 30 50 10 20

Sample Output
3
```
Answer
```
let ar=[10, 20, 20, 10, 10, 30, 50, 10, 20]

function sockMerchant(n, ar) {

    let map={}
    let matchCount=0

    for(let i of ar){
        map[i]=(map[i]||0)+1
    }

    for(let i in map){
        matchCount += Math.floor(map[i]/2)
        console.log(i)
    }
    console.log(map)
    console.log(matchCount)
    }


sockMerchant(10,ar)

```
Question2 ：Get the number of 'a' in repeated times of string 
```
Sample Input
aba
10

Sample Output
7
```
Answer
```
let s='aba'
10

function repeatedString(s, n) {
    let countA=0;
    let countB=0;
    let length=s.length;
    let repeatedTimes=Math.floor(n/length);
    let remainder=n%length;
  
    for(let i of s){
        if(i==='a'){
            countA+=1
        }
    }

    for(let i=0;i<remainder;i++){
        if(s.charAt(i)==='a'){
            countB+=1   
        }
    }

    if(n/s.length===0){
        return countA*repeatedTimes
    }else{
        return countA*repeatedTimes+countB
    } 

}

```


