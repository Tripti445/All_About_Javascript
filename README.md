# 1 : Arrays
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

   
# 2: Objects in Javascript

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

# 3 : ES6 Javascript (var vs let vs const)
=> The makers of Javascript created 2 versions of Javascript ES5 that was till 2015. In 2015 the makers introduced a new version of Javascript known as ES6. In ES5 there was only var keyword to initialize variables. But in ES6 let and const keywords were introduced to create variables, so in ES6 version there is only let and const but not var but In Browser it supports both combination of ES5 and ES6 because of which we are able to use all 3 var, let and const to declare variables.

### Point of Difference between Var and Let keywords : 
1 : Var Existed in older Version of Javascript whereas Let was introduced in the new version of Javascript i.e. ES6.

2 : Var has function scope, whereas Let has braces Scope. 
