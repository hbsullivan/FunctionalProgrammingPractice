/*

deduping

remove duplicates from array, don't use filter()
with/ w/o recursion 

input: [7, 9, "hi", 12, "hi", 7, 53]
output: [7, 9, "hi", 12, 53]

input: [1, 2, 3, 2, 1]
output: [1, 2, 3]

edge case: string, integer

input []
create new [] to store elements that aren't dupes

loop through input
check whether index in already present in new []
if index isn't in new[] push index into new[]
return new[]

*/

let input = 700;

function removeDupes(inputArray) {
    
    <!-- if (typeof(inputArray) === string ||  typeof(inputArray) === integer){
        
        return "is not valid";
        
    } -->
 
    let newArray = []; //newArray = [7, 9, "hi", 12]
    
    for(let i = 0; i < inputArray.length; i++) { //7
        
         if(!newArray.includes(inputArray[i])) {
             
             newArray.push(inputArray[i]);
             
      
        
        }
        
    }
    
    
    return newArray;
}

console.log(removeDupes(input));



//filter array
//if index of the element of array 

//[7, 9, "hi", 12, 7]

  function removeWithFilter(input) {
      
   return input.filter((element, index) => input.indexOf(element) === index);   
      
      
  }

