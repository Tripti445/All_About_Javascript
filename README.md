# 1 : Word vs Keyword
=> any word that is identified by javascript and has a predefined usage in the language is known as a keyword (ex. is, and, for) and any word other than 
   the keyword which is not identified by javascript is called a normal word (ex. papa, chacha, hello)

# 2 : Variables vs Const
=> variable is used to store a value in javascript which can change as per the requirement in future whereas a constant is used to store a value whose value will remain same
   throughout the program and cannot be changed.

# 3 : Hoisting
=>  In Javascript we can use a variable or a function even before it is declared. This process or feature in JS is called Hoisting. In this process javascript's compiler brings 
    the declaration code of the variable or a function to the top of the program behind the scene.

    Ex. console.log(var1);
        let var1;
	
# 4 : Types in JS
=>  There are two types in JS -> Primitives and Reference

<b>Primitives</b> -> null undefined Boolean 

<b>Reference</b> -> [ ], { }, ( ) (brackets are reference type)
    
** Reference type values are those values which when copied to other variable then the original one gets copied, which once changed in other variable affects the same in the original variable also **

    Ex. let a = [1,2,3,4]
        let b = a; 
        b.pop();
        now a and b both will be [1,2,3]
	Because of this behaviour of reference type we usually don't copy the reference type using above logic i.e. b = a instead we write b = [...a] 

** Primitives are opposite of Reference type, when primitived get copied their duplicate value are copied, which if changed in other variable, it does not affect the original variable. **

    Ex. let a = 12;
        let b = a;
        b = b+2;
        now a is 12 and b is 14; 

# 5 : Conditionals in JS
=> Conditionals in JS are used to specify a condition for a particular part of the program to run, if it satisfies the condition. 

   The conditionals accept only 2 types of value : Truthy and Falsy.
   
    Ex. if(11>12)      ** here the conditions converts to false, hence the Else part of code will run
         {
 	     xyz;
	 }
       else
	{
             wxy;
        }

# 6 : Loops
=> Loops are used to repeat a code n number of times based on the loop condition without repeatedly writing the code. 3 loops are present in JS :

   1: For Loop
   
   2: While Loop
   
   3: Do-While Loop

# 7 : Functions in JS

=> Function is particulary naming a piece of code which can be used any time with any data and any number of time. Functions in JS are mainly for 3 usecases : 

   1 : When you don't want to run the particular code right now but after sometime in future
   
   2 : When you want to reuse the code
   
   3 : When you want to run a particular code with different data everytime.



	
# 8 : Arrays
=> Arrays in Javascript are used to store more than one value. Ex. [1,2,3,4]. There are various operations performed on arrays

   i) Pop -> Pop is used to remove last element of the array. The popped array can also be stored in a variable.
   
   ii) Push -> Push is used to append an element in the array.
   
   iii) Shift -> Shift method is used to remove the element at the first index of the array and shift the rest elements to the lower index. Shift method also return the element removed
   
                 Ex. arr= [1,2,3,4] -> after arr.shift() -> [2,3,4]

   iv) Unshift -> Unshift method is used to add an element at the starting position of the array and unshifts the older elements to higher index
   
                 Ex. arr = [1,2,3,4] -> after arr.unshift(7) -> [7,1,2,3,4]

   v) Splice -> Splice method is used to add or remove elements from the array based on parameters passed in the array
   
                Ex. const fruits = ["Banana", "Orange", "Apple", "Mango"];
                    fruits.splice(2, 0, "Lemon", "Kiwi");
                    Output : ["Banana","Orange","Lemon","Kiwi","Apple","Mango"]
                    
                 Here in the above example 2 represents the index from where the elements will be added
                    0 represents the number of elements to be removed 
                    "Lemon" and "Kiwi" are the elements which are to be added
                 ** If you don't mention the elements to be added it will delete the items as per the parameters passed

   vi) Slice -> The slice() method slices out a piece of an array into a new array
   
                Ex. const arr= [1,2,3,4]
                    arr.slice(1) -> [2,3,4]

   
# 9: Objects in Javascript

=> When we talk about more than one element we called it an array. But when we talk about a single element in detail we represent it as an object. Objects means to store details 
   of a single individual.
   
   ** Empty Object : 
      const obj1 = {}

   ** Filled Object : 
      const obj1 = {
		name : "Ruchit",
		age : 22,
		company : "HSBC"
	}
 
   Objects basically contains key value pairs, where keys are referred to as "Properties". Objects also contain methods whose value is a function. We can change the values of objects 
   obj1.name = "Harsh";

# 10 : ES6 Javascript (var vs let vs const)
=> The makers of Javascript created 2 versions of Javascript ES5 that was till 2015. In 2015 the makers introduced a new version of Javascript known as ES6. In ES5 there was only var keyword to initialize variables. But in ES6 let and const keywords were introduced to create variables, so in ES6 version there is only let and const but not var but In Browser it supports both combination of ES5 and ES6 because of which we are able to use all 3 var, let and const to declare variables.

### Point of Difference between Var and Let keywords : 
1 : Var Existed in older Version of Javascript whereas Let was introduced in the new version of Javascript i.e. ES6.

2 : Var has function scope that means Var can be used anywhere inside it's parent function's scope.
    
    Ex. function test()
    	{
     	   for(var i=0;i<10;i++)
	       {
               console.log(i);
	        }
            console.log(i)
	 }
     Here we can even print i outside the loop because it was declare using a Var keyword and var is valid anywhere inside the function scope, which in most programming language gives error.

 To tackle the above property Let keyword was introduced which has a braces scope. It means it is only valid inside the curly braces under a loop or a conditional. In example we can say that in the above example
 if we would have declared a variable i with Let then outside the loop the console.log(i) would have given an error because let has only braces scope so it will only exist inside the loop above.

 3 : Var adds itself to the window object. It means any variable declared with Var gets added to window object which exposes to 3rd party api which is not safe. So this thing was removed in Let.

 # 11 : Window Object
 => There are many features which we use to develop websites which are not provided by javascript but are provided by the Browser. All these feature which are not the part of JS , we can find them in an object provided by the Browser known as Window Object. Window object is like a box of features which is JS uses to implement various things.

 # 12 : Stack Memory and Heap Memory
 => Stack memory in Javascript is used to store the execution order of multiple function. If we use nested functions in a program they get added to the stack and later they are executed based on Last In First Out order. Heap Memory is used to store the variables and date during execution.

 # 13 : Execution Context
 => Execution Context is basically when we execute a function, then it will create it's own imaginary container where there will be 3 things : 
 
1 : variables

2 : functions inside that parent function

3 : lexical environment

 	Ex. function abcd() 
  	    {
               var a = 2;
	       function def()
		{
  			var x = 5;
  		}
    	    }
In the above example, when the function abcd() will get executed it's execution context will be created and inside that var a and function def() will be stored. But var x will not be stored because var has function scope and variable x's parent is def(), so it can't be accessed outside the function def(). This property is called Lexical Scope or Lexical Environment, which decides that a function can access what values. The lexical scope exists where there is a scope chain, i.e. a chain of nested functions.

# 14 : How to Copy Reference Type Values
=> As we have studied earlier that if we directly copy a reference type value in another variable. Ex. const a = [1,2,3,4] and b = a, then it will copy the original array and if we make any changes to the original array then the copied array will also be modified. So to tackle this we copy a reference type value using a Spred Operator.

	Ex. const a = [1,2,3,4,5]
            const b = [...a]

     Using a spread operator the values of the original gets unpacked and we can store them anywhere.

Similary we copy objects in javascript using same spread operator. 

 	Ex. const a = { 
  			name : "Ruchit",
     			age : 21
	 	      }
	 const b = {...a}

# 15 Truthy vs Falsy Values
  => In Javascript whatever we write is basically one out of two things. Either the value is Truthy or Falsy.
  
  <b>Falsy Values : </b> 0, False, undefined, Null, NaN, document.all

  All values other than Falsy values are Truthy. So if we put any Falsy value in a conditional statement then the else part of the condition runs, and if we put a Truthy value in a conditional then the If part of the conditional will execute.

  	Ex. if(1)
   		{
         	  console.log("Hello");
	    	}
	    else
     		{
       		  console.log("Bye");
	        }
	Since 1 is a Truthy value so it will give output as "Hello"

# 16 forEach() Loop
=> forEach Loop can be used only in Array. For Each loop is used to apply a function to every value in the array

	Ex. const arr= [1,2,3,4,5,6];

	    arr.forEach(function(val)=>{
     		console.log(val+2);
            })
  forEach loop does not make changes in the original array, but makes the changes in the temporary copy of the array. The values that get passed to the function inside forEach loop does not actually gets copies, but it's temp copy is passed.
                        
# 17 For in Loop
=> For In loop can only be used in Javascript Objects. 

	Ex. const obj1 = {
                           name : "Ruchit",
			   age : 23,
                           company : "HSBC"
		         }
	   
	 for(var key in obj1)
        {
		console.log(obj1[key]);
	}

 
