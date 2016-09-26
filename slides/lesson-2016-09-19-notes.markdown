
# Program structure

- Expressions and statements
- Variables


- The environment
- Functions
- The console.log function
- Return values
- Prompt and confirm


- Control flow
- Conditional execution
- While and do loops
- For loops
- Breaking out of a loop


- Updating variables succinctly
- Dispatching on a value with switch

- Keywords and Reserved words

- Indenting code
- Capitalization
- Comments



















Split the monitor between browser/console and vi...
















## Expressions! Sub expressions!

First version. Two expressions, neither does anything:

    365 * 24 * 60 * 60;
    365 * 24 * 60 * 60 / 12;











Second version. Include the numbers in strings (sub-expressions), still just expressions, so they don't do anything:

    "There are (usually) " + (365 * 24 * 60 * 60) + " seconds in a year!"
    "That means that there is (usually) on average " + (365 * 24 * 60 * 60 / 12) + " seconds per month!"





































## Statements!

Third version. Now, two statements. Each prints out one of the numbers:

    console.log("There are (usually) " + (365 * 24 * 60 * 60) + " + seconds in a year!");
    console.log("That means that there is (usually) on average " + (365 * 24 * 60 * 60 / 12) + " seconds per month!");























## Variables!
## Makes it easier to see what's going on, even when the values don't change:

Fourth version. Simplify with variables. Use the variables as expressions:

    var days_per_year = 365;
    var hours_per_year = days_per_year * 24; 
    var minutes_per_year = hours_per_year * 60;
    var seconds_per_year = minutes_per_year * 60;
    var seconds_per_month = seconds_per_year / 12;

    console.log("There are (usually) " + seconds_per_year + " seconds in a year!");
    console.log("That means that there is (usually) on average " + seconds_per_month + " seconds per month!");
























## Capitalization!

## Pop quiz, what happens to `a` here:

    var a = 10;
    var b = a;
    b = b + 1;

What is a? What is b?

`a` is unchanged! Variables just "point" to the value! The third line makes b point to something new, doesn't change the thing it pointed to before!

























## Comments!
    

    // This is obviously not always true...
    var days_per_year = 365;
    var hours_per_year = days_per_year * 24; 
    var minutes_per_year = hours_per_year * 60;

    /* This is surprisingly also not always true!
       Leap-seconds! Way worse than leap-years!
       Little shits sneak up on you... :(
       Note: You can't use multi-line comments in the browser console, except when pasting!
    */
    var seconds_per_year = minutes_per_year * 60;
    var seconds_per_month = seconds_per_year / 12;

    console.log("There are (usually) " + seconds_per_year + " seconds in a year!");
    console.log("That means that there is (usually) on average " + seconds_per_month + " seconds per month!");
























## Looping, let's start with a little exercise, and see if you know enough about looping to solve it already!
## Exercise: Let's print out a 10x10 square of X's in the console, along with the number of the row at the end of each line, like this:


XXXXXXXXXX 1
XXXXXXXXXX 2
XXXXXXXXXX 3
XXXXXXXXXX 4
XXXXXXXXXX 5
XXXXXXXXXX 6
XXXXXXXXXX 7
XXXXXXXXXX 8
XXXXXXXXXX 9
XXXXXXXXXX 10

(doesn't look very square, because the letters aren't square either; doesnt matter!)


My amazing solution!!:



























    console.log('XXXXXXXXXX 1');
    console.log('XXXXXXXXXX 2');
    console.log('XXXXXXXXXX 3');
    console.log('XXXXXXXXXX 4');
    console.log('XXXXXXXXXX 5');
    console.log('XXXXXXXXXX 6');
    console.log('XXXXXXXXXX 7');
    console.log('XXXXXXXXXX 8');
    console.log('XXXXXXXXXX 9');
    console.log('XXXXXXXXXX 10');

## Let's make that a little simpler, by using a for loop, to do this ten times for us:

    for (var i = 1; i <= 10; i = i + 1) {
        console.log('XXXXXXXXXX ' + i);
    }


























## So, what does that actually do:

    for (INIT-STATEMENTS ; TEST-EXPRESSIONS ; UPDATE-STATEMENT) {
        BODY-STATEMENTS
    }

    means: 

        var i = 1; // pretty simple. We could have set up the variable before the for loop. Makes no difference!
        
        // CHECK THAT i is less than or equat to 10. The for loop is over if it isn't!

        console.log('XXXXXXXXXX ' + i);

        i = i + 1

        // JUMP BACK to the `CHECK THAT` line!

























## Still, looks stupid with having those ten X's in the `console.log` line. Let's do this with a `while` loop:

    var xs = '';

    while (xs.length < 10) {
        xs = xs + 'X';
    }
    
    for (var i = 1; i <= 10; i = i + 1) {
        console.log(xs + ' ' + i);
    }
























## do { ... } while(...)

























## Indentation!


























## Exercise: Let's change row 5 to use Ys instead of Xs, like this:


XXXXXXXXXX 1
XXXXXXXXXX 2
XXXXXXXXXX 3
XXXXXXXXXX 4
YYYYYYYYYY 5
XXXXXXXXXX 6
XXXXXXXXXX 7
XXXXXXXXXX 8
XXXXXXXXXX 9
XXXXXXXXXX 10


My amazing solution:

















    console.log('XXXXXXXXXX 1');
    console.log('XXXXXXXXXX 2');
    console.log('XXXXXXXXXX 3');
    console.log('XXXXXXXXXX 4');
    console.log('YYYYYYYYYY 5');
    console.log('XXXXXXXXXX 6');
    console.log('XXXXXXXXXX 7');
    console.log('XXXXXXXXXX 8');
    console.log('XXXXXXXXXX 9');
    console.log('XXXXXXXXXX 10');

















## if/else (use plenty of time here, check that everybody gets the "tests"!!):

    var xs = '';
    var ys = '';

    while (xs.length < 10) {
        xs = xs + 'X';
        ys = ys + 'Y';
    }
    
    for (var i = 1; i <= 10; i = i + 1) {
        if (i === 5) {
            console.log(ys + ' ' + i);
        } else {
            console.log(xs + ' ' + i);
        }
    }

























## Now, let's make line 7 completely empty, (if/else if/else):

    var xs = '';
    var ys = '';

    while (xs.length < 10) {
        xs = xs + 'X';
        ys = ys + 'Y';
    }
    
    for (var i = 1; i <= 10; i = i + 1) {
        if (i === 5) {
            console.log(ys + ' ' + i);
        } else if (i === 7) {
            console.log("");
        } else {
            console.log(xs + ' ' + i);
        }
    }
















## Simpler way of updating variables += /=, etc.


    var xs = '';
    var ys = '';

    while (xs.length < 10) {
        xs += 'X';
        ys += 'Y';
    }
    
    for (var i = 1; i <= 10; i = i + 1) {
        if (i === 5) {
            console.log(ys + ' ' + i);
        } else if (i === 7) {
            console.log("");
        } else {
            console.log(xs + ' ' + i);
        }
    }












## break/continue
















## Prompt, functions, return values, break:

    var xs = '';
    var ys = '';

    while (xs.length < 10) {
        xs += 'X';
        ys += 'Y';
    }
    
    for (var i = 1; i <= 10; i = i + 1) {
        if (i === 5) {
            console.log(ys + ' ' + i);
        } else if (i === 7) {
            console.log("");
        } else if (i === 2) {
            if (confirm('should we just stop now?')) {
                break;
            }
        } else {
            console.log(xs + ' ' + i);
        }
    }




















## Let's wrap this in our own function, so we can call it again and again!

    var print_square = function(rows, columns) {
        var xs = '';
        var ys = '';

        while (xs.length < columns) {
            xs += 'X';
            ys += 'Y';
        }
        
        for (var i = 1; i <= rows; i = i + 1) {
            if (i === 5) {
                console.log(ys + ' ' + i);
            } else if (i === 7) {
                console.log("");
            } else if (i === 2) {
                if (confirm('should we just stop now?')) {
                    break;
                }
            } else {
                console.log(xs + ' ' + i);
            }
        }
    };

















## Alternative function syntax

## Use what we now know to dissect our jQuery code from last week!


