Without Recursion:

function replace(input) {
    let result = "";
    for (let i = 0; i < input.length; i++) {
        if (input[i] === " ") {
            result += "%20";
        } else {
            result += input[i];
        }
    }
    return result;
}



With Recursion:

function replaceWithRecursion(inputString) {
    if (inputString.length === 0) {
        return "";
    }
    if (inputString[0] === " ") {
        return "%20" + replaceWithRecursion(inputString.substring(1));
    }
    return inputString[0] + replaceWithRecursion(inputString.substring(1));
}
