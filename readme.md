  JavaScript Assignment-8

1. Write short notes on the below with code examples
while loop :- 

The while loop repeats a block of code as long as a specified condition is true.
~~~js
let i = 0;
while (i < 5) {
    console.log("The number is " + i);
    i++;
}
/*output : The number is 0
           The number is 1
           The number is 2
           The number is 3
           The number is 4 */
~~~

do-while loop :-

The do-while loop is similar to the while loop, but it will always execute the block of code once before checking the condition.
~~~js 
let i = 0;
do {
    console.log("The number is " + i);
    i++;
} while (i < 5);

/* output : The number is 0
            The number is 1
            The number is 2
            The number is 3
            The number is 4*/
~~~
for loop :-

The for loop is used when you know in advance how many times you want to execute a statement or a block of statements.
~~~js
for (let i = 0; i < 5; i++) {
    console.log("The number is " + i);
}
/* output : The number is 0
            The number is 1
            The number is 2
            The number is 3
            The number is 4*/
~~~

for in loop :-

The for in loop iterates over the properties of an object.
~~~js
const person = {fname: "Ashley", lname: "Doe", age: 25};

for (let key in person) {
    console.log(key + ": " + person[key]);
}
/* output : fname: Ashley
            lname: Doe
            age: 25*/
~~~
for of loop :-

The for of loop iterates over the values of an iterable object (like an array or a string).
~~~js
const cars = ["Volvo", "BMW", "Mini"];

for (let car of cars) {
    console.log(car);
}
/* output : Volvo
            BMW
            Mini*/
 ~~~
2. write a function that takes an array of numbers as an argument and returns the sum of its elements ?
~~~js
    let sum = 0;
    let sumofelements = (input) => {
        for ( i = 0; i <= input.length; i++) {
            sum += i; 
                                     
                }
                return sum; 
            }
        
    console.log(sumofelements(arr));
    
    /*output : 15*/
    ~~~
 3. Create a function that filters strings in an array by their length
 ~~~js
 function filterArray() {
        let arr = ['mango', 'orange', 'apple', 'grape','date','lime','pear'];
        let filteredArr = arr.filter(item => item.length <= 4);
        
        return filteredArr; 
    }
    
    console.log(filterArray()); // output : [ 'date', 'lime', 'pear' ]   
 ~~~
 4. Create a function that returns a new array containing the square roots of each number in the original array [1,4,9,16,25] (Math.sqrt())
 ~~~js
  function SquareRoots(arr) {
        return arr.map(Math.sqrt);
    }
    let Array = [1, 4, 9, 16, 25];
    let NewArray = SquareRoots(Array);
    
    console.log(NewArray); // Output: [1, 2, 3, 4, 5] 
 ~~~

5. Create an array with 5 student’s names. Then create a function that takes two parameters (allStudents and studentName). Iterate over all the students and find that specific user ‘studentName’
~~~js
let allStudents = ["Alice", "Bob", "Charlie", "David", "Eva"];
function findStudent(allStudents, studentName) {
    for (i = 0; i < allStudents.length; i++) {
        if (allStudents[i]=== studentName) {
            return true;
        }
    }
    return  false;
}
let result = findStudent(allStudents, "john");
console.log(result);// output : false
~~~ 
Write a function that prints the number 1 to 100. But for multiples of 3, print Fizz instead of the number, and for multiples of 5, print Buzz. For the numbers that are multiples of both 3 and 5, print FizzBuzz(use while loop)
~~~js
function fizzBuzz() {
    let i = 1; 
    while (i <= 100) { 
        if (i % 3 === 0 && i % 5 === 0) {
            console.log("FizzBuzz");
        } else if (i % 3 === 0) {
            console.log("Fizz");
        } else if (i % 5 === 0) {
            console.log("Buzz");
        } else {
            console.log(i);
        }
        i++;
    }
}
fizzBuzz();
/*output :
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
...

*/
~~~