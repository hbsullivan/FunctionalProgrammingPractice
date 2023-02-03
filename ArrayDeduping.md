Without recursion: 

function removeDupe(inputArray) {
    let newArray = [];
    for (let i = 0; i < inputArray.length; i++) {
        if (!newArray.includes(inputArray[i])) {
            newArray.push(inputArray[i]);
        }
    }
    return newArray;
}



With Recursion: 


function removeDuplicatesRecursive(input, result = []) {

  
  if (input.length === 0) {
    return result;
  }

  let newIndex = input[0];

  if (!result.includes(newIndex)) {
    result.push(newIndex);
  }

  return removeDuplicatesRecursive(input.slice(1), result);
}



With filter(): 

function removeDuplicates(array) {
  return array.filter((item, index) => array.indexOf(item) === index);
}
