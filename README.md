# Algo-SteamRoller
Steamroller : Flatten a nested array. You must account for varying levels of nesting.

```javascript
function steamrollArray(arr) {
  // I'm a steamroller, baby
    var flattenArray=[];
    //Function to introduce in foreach
    var flatten=function(arg){
       if (!Array.isArray(arg)){
           flattenArray.push(arg);
       }else{
           for(var a in arg ){
             
              flatten(arg[a]);
           }
       }
    }
    //forEach
  arr.forEach(flatten);
  return flattenArray;
}

console.log(steamrollArray([1, [2], [3, [[4]]]])); 
console.log(steamrollArray([[["a"]], [["b"]]]));
```
