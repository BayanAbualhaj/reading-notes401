# Node Ecosystem, TDD, CI/CD

![TDD](http://19yw4b240vb03ws8qm25h366-wpengine.netdna-ssl.com/wp-content/uploads/Test-driven-development-cycle-Cybus-Nordic-APIs.png)
![CI/CD](https://wpblog.semaphoreci.com/wp-content/uploads/2020/02/cic-cd-explained.jpg)

____________

## Array.map():

* The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
* map calls a provided callback function once for each element in an array, in order, and constructs a new array from the results. callback is invoked only for indexes of the array which have assigned values (including undefined).


## Array.reduce():
* The reduce() method executes a reducer function (that you provide) on each element of the array, resulting in single output value.
* The reducer function takes four arguments:
    - Accumulator
    - Current Value
    - Current Index
    - Source Array
* Your reducer function's returned value is assigned to the accumulator, whose value is remembered across each iteration throughout the array, and ultimately becomes the final, single resulting value.

____________

***superagent():***

![57](https://github.com/BayanAbualhaj/reading-notes401/blob/master/img/Screenshot%20(79).png?raw=true)


______________________

***what is a promise?***:
a promise in programming is telling the code to **NOT** run until the function who called the promise is fully run, in simple words the first function need time to fully run and the second function is lighter(need less time) but it needs the information from the first function and because when reading the code the code order it self and then run and maybe without the promises the code will be damaged. 


so that part of the code (promise) will run after the function that called it a promise 


***callback functions***
No they are not all asynchronous because callback function is a regular function it's act in the way it called if it's call in an asynchronous way it will act async if its called in synchronous way it will act sync. 


![async](https://res.cloudinary.com/practicaldev/image/fetch/s--5e204O-Y--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/rjqf7w2vmlxxz5ez0dbz.png)



![sync](https://res.cloudinary.com/practicaldev/image/fetch/s--dqZaqp09--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/hyaxexxqnkl9ymxrjlh4.png)



[follow this link for more ^_^](https://dev.to/marek/are-callbacks-always-asynchronous-bah)


