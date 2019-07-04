# hackerrank

Question1 ：Get the number of max match
```
Sample Input
9
10 20 20 10 10 30 50 10 20

Sample Output
3
```
Answer:
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
Answer:
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


```
Question3 ：Get the number of step when jump from the start to end of an array 
The array consist of 0 and 1,0 means you the step you can jump while 1 means the obstacle need to be avoided.
You can take 1 or 2 step each time.
```
Sample Input
aba
10

Sample Output
7
```

Answer:
```
let c=[0, 1, 0, 0, 0, 1, 0]
c=[0, 0, 1, 0, 0 ,1 ,0]
c=[0, 0, 0, 1, 0, 0]

function jumpingOnClouds(c) {
    let count=0;
    let currentIndex=0;

    while(currentIndex<c.length-1){
        if(c[currentIndex+1]===0){
            if(c[currentIndex+2]===0){
                count+=1
                currentIndex+=2
            }else{
                count+=1
                currentIndex+=1
            }
        }else{
            if (c[currentIndex+2]===0){
                count+=1
                currentIndex+=2
            }
        }
        
    }
  
    // console.log('currentIndex',currentIndex)
   return count

}

jumpingOnClouds(c) 
```