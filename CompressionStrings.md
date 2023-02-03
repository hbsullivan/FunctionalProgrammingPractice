Without recursion: 

function compress(input) {
    let result = "";
    let counter = 1;
    for (let i = 0; i < input.length; i++) {
        if (input[i] === input[i + 1]) {
            counter++;
        } else {
            if(counter === 1){
              counter = "";
              result += counter + input[i];
              counter = 1;
            } else{
              
              result += counter + input[i];
              counter = 1;
            }
        }
    }
    return result;
}


With Recursion: 

function compressWithRecursion(input) {
  if (input.length === 0) {
    
  return "";
  } 
  
  let count = 1;
  let i = 1;
  while (i < input.length && input[i] === input[i - 1]) {
    count++;
    i++;
  }
    if(count === 1) {
        count = "";
        return count + input[i - 1] + compressWithRecursion(input.slice(i)); 
        
    }
  
  return count + input[i - 1] + compressWithRecursion(input.slice(i));
}

