# String-repeat-Kata


instructions 


Write a function called repeatStr which repeats the given string string exactly n times.

EXAMPLE:

repeatStr(6, "I") // "IIIIII"


repeatStr(5, "Hello") // "HelloHelloHelloHelloHello"


This is a Simple Kata 8.

Logic behind this. 

We have two parameters and Integer and String, In that order. Integer will define how manytimes we will printout the string.
Here there is not much explanation or logic to do. I am going to give 3 ways to accomplish this Kata but the last one will not work on Codewars.

using While loop:



function repeatStr (n, s) {
  
  var repeatString = "";
  
  while (n > 0) {
    
    repeatString = repeatString + s;
    n--;
    
  }
  
  return repeatString;  
}


Using If statement: 


function repeatString(n, s) {

  if(n < 0) 
  
    return "";
    
  if(n === 1) 
  
    return s;
    
  else 
  
    return s + repeatString(s, n - 1);
    
}

and Finally using repeat method:

function repeatString(n, s) {
  if (n > 0)
    return s.repeat(n);
  else
    return "";
}
return repeatString;

SAME METHOD BUT USING TERNARY OPERATION


n > 0 ? s.repeat(n) : "";
