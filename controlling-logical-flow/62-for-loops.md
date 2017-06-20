# For Loops
The most common kind of loop in any programming language is probably [the `for` loop](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#The_standard_for_loop). This is a structure that allows us to define a clear number of times to loop through some set of instructions. The `for` loop can be used anytime we need to repeat a set of instructions for a specific number of iterations.

Here is an example of a `for` loop in JavaScript:

```js
for(let i=0; i<10; i++) {
    console.log(`This is iteration number ${i}.`);
}
```
The `for` loop structure is not too complex, but it does require a specific syntax to make it happen. First, it identifies as a `for` loop with the keyword `for`. Then we list three statements in the top line of the loop: 

1. **Initializer:** The first statement initializes a counter variable to a value. (This could be any variable name, but the letter `i` for "iteration" is often used.) This is the value where the counter will begin.
2. **Exit Condition:** The second statement provides a conditional assertion that is checked on each iteration of the loop. Each time the loop executes, it checks this assertion to see if it's `true`. If so, the loop continues. If not, the loop stops.
3. **Final Expression:** third statement increments the value of the counter by one. This causes the value of the counter to increase, so eventually the second statement will return `false`.

Here is another example of how a `for` loop can function:

```js
var simpsons = ['Homer', 'Marge', 'Bart', 'Lisa', 'Maggie'];

for (let i=0; i<simpsons.length; i++){
    console.log(simpsons[i]);
}
```
Notice that in this example we are actually using the `i` variable (which is the counter for the `for` loop) as the index for which name we want to output. This code would output each of the names to the JavaScript console in the web browser.


<div class="tip-box">

<h3>Looping Arrays the Old Way</h3>

<p>It used to be necessary to use the standard form of the <code>for</code> loop through Arrays. To do this, we would use the <code>Array.length</code> property to set the exit condition for the loop. This method still works, and it's used in some examples on this page. But pay attention to the more modern way of looping arrays over the next couple of sections of the book.</p>

</div>


{% exercise %}
Define an a `for` loop that would double `foo` 12 times.

{% initial %}
var foo = 2;
for ( ){
    foo = foo * foo;
    console.log(`Foo equals ${foo}.`);
}

{% solution %}
var foo = 2;
for (let i=0; i<12; i++){
    foo = foo * 2;
    console.log(`Foo equals ${foo}.`);
}

{% validation %}
assert(foo==8192, "Incorrect.");

{% endexercise %}
