Without Recursion: 


function unique(input) {
    
    for (let i = 0; i < input.length; i++) {
        
        for (let j = i + 1; j < input.length; j++) {
            
            if (input[i] === input[j]) {
                return false;
            }
        }
    }
    return true;
}




With Recursion: 

function uniqueWithRecursion(input) {
    if (input.length === 1) {        
        return true;       
    }
    for (let i = 1; i < input.length; i++) {
        
        if (input[0] === input[i]) {
            
            return false;
        }
    }
    
    return uniqueWithRecursion(input.slice(1));
}