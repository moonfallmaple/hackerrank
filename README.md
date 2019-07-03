# hackerrank

Question1 ：Get the number of max match
```
Sample Input
9
10 20 20 10 10 30 50 10 20

Sample Output
3
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






