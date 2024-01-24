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
		console.log(obj1[key]);     # output - "Ruchit", 23, "HSBC"
	    }

# 18 Do-While Loop
=> Do-While loop is different from While Loop because in Do-While loop, the Do part is executed first even before first time while condition is checked. This means that whether the condition matches or not, in Do-While the Do part will execute atleast once.

	Ex. var a=120;

         do
	     {
           console.log("Hey");
           a++;
	     }
        while(a<15);

     # Here the condition is false but still atleast once "Hey" will get printed.

# 19 Callback Functions
=> In Javascript when there is a part of code that is planned to execute after sometime and that time is not confirmed or confirmed, such part of code is kept inside a callback function which is used to execute that part of code after set or unset time. This callback function is part of Asynchronous Javascript. For ex. If there is a button to bring an image from Facebook Server, after clicking the button we don't know how much time the process will take. In this case we will use callback function which will notify us when the process is completed so that we can execute further part of the code after the facebook image execution is completed.

 	Ex. setTimeOut(function(){
  		console.log("Hello Callback Function");
    		},2000)
      
       # In above code the setTimeOut is a callback function which executes the passed function after the set time, in above case 2 seconds.

# 20 First Class Functions
=> In Javascript there is a feature that we can use a function as a value or we can pass function as a parameter to another function because in JS the functions are first class functions

	Ex. 1 
 		var a = function() {
   				 console.log("First Class Function");
				}

    	Ex. 2  function abcd(a)
                  {
	                a();
                  }

               abcd(function(){console.log("Fist Class Function")});

# 21 How Arrays are Made Behind the Scenes
=> In Javascript arrays are actually Objects. If we write typeOf([]) , it will give output as "object". 

 	Ex. var a= [1,2,3,4]

	Javascript stores the above array as follows

  	var a = {
   		0 : 1,
            2 : 2,
	        3 : 3,
            4 : 4,
	        }

       We can make negative index in the array also
       a[-1] = 99;

       Output : [ 1, 2, 3, 4, '-1': 99 ]

# 22 How to Delete Object keys 
=> In Javascript we can delete the object key:value entirely from the object memory

 	Ex. const obj = {
                    name : "Ruchit",
			age : 22
                    }

             delete obj.age;

          Output : {name : "Ruchit"}

# 23 Higher Order Functions
=> Higher Order Functions are those functions which accept a function as it's parameter.

 	Ex. function abcd(val)
                     {
		       val()
	             }
	   abcd(function(){console.log("Higher Order")})   # This is a Higher Order Function because it accepts another function as it's parameter

       Ex. Javascript has some pre defined higher order functions. ForEach, setTimeOut, etc.
       		const arr = [1,2,3,4]
	        arr.forEach(function(val)(
	 		val = val+1;
	        ))
	 Here in the above example forEach passes another function as it's parameter, so forEach is a Higher Order Function.
		
 # 24 Constructor Functions
 => Constructor functions are those functions which requires a "new" keyword during it's declaration and uses "this" keyword inside the function. Ex. in a Biscuit Factory, there is a mould which has some fixed properties and that mould presses the batter and creates 
    similar bisuits having property that of the mould. The mould in this case is the constructor function and the biscuits produced are the instances of that function.

    	Ex. function mould() 
             {
	         this.width = 12;
	  	 this.height = 22;
             this.color = "Brown";
		 this.taste = "sweet";
            }
         let bisuit1 = new mould();    # here the bisuit1 is the instance of the constructor function mould(). It has all the properties defined inside the mould function.
In short we can say that we use a constructor function when you want to create multiple elements of the same type.

# 25 New Keyword
=> Whenever the "New" keyword is used, it represents an empty object with the name "this" keyword.

 	Ex. function abcd()
  	  {
             this.name= "Ruchit";
	  }
   
          new abcd()  # by using "new" keyword here we create an empty object
	  {
            name : "Ruchit"
	  }
# 26 IIFE
=> Immediately Invoked Function Expression is the art of immediately exectuing the function in such a way that we are able to create a private variable which can't be changed and cant' be accessed. It is basically created to make a variable safe from getting changed from outside soruce. We create a Getter and Setter method to access and change the value of the private variable.

 	    var a = ( function(){
	    var privateVal = 12;
	    
	    return {
	        getter: function(){
	            console.log(privateVal);
	        },
	        setter : function(val){
	            privateVal = val;
	        }
	    }
	})()
	
	a.setter(14);
	
	a.getter()

 # 27 Prototypes
 => If we create an object and then put a "." after the object name in the console, then it will start showing some properties of the object which were not defined by ther user. Ex. ".length()". So these properties were created by the java developers which has some predefined properties for every object created in JS. These predefined helper properties and methods present in every object in JS is stored in that object's prototype. 

 # 28 Prototype Inheritance
 => Like every child inherit some properties of it's parents and has some additional properties in himself, similary in JS objects we can inherit some properties of other object known as parent object.

  	Ex. const Human = {              # parent object having basic properties of a human being
   		canTalk : true,
     		canWalk : true,
       		hasFourLegs : false,
	 	haveEmotions : true
             }

            const Student = {            # child object having some additional properties above basic human being
	    	canStudy = true,
      		canSolveProblems : true,
		canRead : true,
	     }

      	    Student.__proto__ = Human;  # syntax to inherit properties from Parent object i.e. Human 

    # Now we can access the properties of Human object from Student object because we have inherited them and now they are the part of Student object Protoype.

# 29 "This" Keyword
=>  When we write anything outside {} brackets then we say that the code is in the Global Scope. If we use "this" keyword in the Global Scope then it returns the <b>Window</b> object. In the Function scope i.e. inside a function also "This" keyword returns a window object. A function inside an object is called "Method". Inside a method the value of "this" keyword will refer to the parent object itself.

 	Ex. const obj1 = {
                 name : "Ruchit",
		 speak : function abcd(){
    			console.log(this)
       			}
  		}
           obj1.speak();  # it will give output as the object obj1 itself

   	In DOM Manipulation, if we are using an addEventListener to a button, and inside the even listener if we add "this" , then "this" will refer to the button object and can be used to mnaipulate it's properties.

     	Ex. button.addEventListener(function(){
      		this.style.color = "red";
		})
  	Here 'this' keyword will represent the button object and can manipualte the color of the button.
# 30 Call, Apply, Bind
=> <b>Call : </b> When you have a function and an object and you have to execute the function and by default the value of "this" keyword inside the function scope is the window object, that we need to change and instead we need to make it point to an object then we use call method.

 	Ex. function abcd() {
  		console.log(this.age)
    		}
               var obj = {age : 24}
	           abcd.call(obj)

            If we have to pass some parameters in call function.
	    	function abcd(val1,val2,val3){
      			  console.log(this,val1,val2,val3)
      			}
	 		var obj = {age:24}
     			abcd.call(obj,1,2,3)  # this will give output as {age:24},1,2,3
<b>Apply : </b> In Apply method we have the same process like in Call, but the difference is that in Call where we were passing arguments separately, in apply we pass an array for multiple values

   	Ex. function abcd(val1,val2,val3){
      			  console.log(this,val1,val2,val3)
      			}
	 		var obj = {age:24}
     			abcd.call(obj,[1,2,3])  # this will give output as {age:24},1,2,3
<b>Bind : </b> Bind is used to bind a function and an object and save it in a variable and use that Binded Object and Function for later use. Sometimes we want the object and function not to be executed immediately, instead after some event has happened like a button is clicked. At that time we used this binded object and function created using Bind method

 	Ex. Ex. function abcd() {
  		console.log(this.age)
    		}
               var obj = {age : 24}
	           var bindedObj = abcd.bind(obj)

 # 31 Pure and Impure Function
 => In Javascript a function is said to be a Pure Function if it has any of the following properties : 
 
 1 : For same input in a function it should give the same output everytime. (but in Math.random(), even if you give same input it will give different output everytime, so it is an impure function)
  
 2 : It should never change the value of the variables in the global scope.

 # 32 Synchronous and Asynchronous Javascript
 => <b>Synchronous vs Asynchronous : </b>: When we execute the code sequentially meaning that until and unless the first part of code doesn't gives an output the execution doesn't moves to execute the other part of the code. Whereas in Async, multiple tasks start to execute together and the part which gives the anwer first gets executed first. 

	ex. Task a - 3
 	    Task b - 5
      	    Task c - 15
	    Task d - 2
     In above sequence in sync execution , first task A will run , once A gets completed, only then B will start executing, once B gets executed then C will get executed and then D will execute.

     In Async execution, first all the four tasks will start at the same time, first the task D will complete it's execution coz its taking smallest time, then after 1 sec task A will give it's output, similary after sometime tasks B and C will give their answer. So overall Async execution will take less time than Synch execution, coz here tasks executes parallely.

<b>How to know if we are writing Asynchronous Code </b> : If we are using setTimeOut, setTimeInterval, Promises,fetch, axios, XMLHttpRequest. These methods are asynchronous.

<b>Asynchronous Javascript : </b>By Default Javascript is Synchronous in nature which means it executes a code sequentially. But if in between the code there is a server request which will take some amount of time to get the response from the server, and the execution time is not confirmed then in that case we use async javascipt to execute that line. Because if we will not use async there then the further line of code will execute before the previous line will get the response and return the ans.
     
 		
   
