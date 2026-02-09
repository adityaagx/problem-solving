07 - Functions (Doing One Thing Properly)

Up to now, you’ve learned how to think in:

* Steps
* State
* Actions
* Conditions
* Loops

Now comes a very important idea.

As a programmer, you don’t want to:

* Repeat the same thinking again and again
* Rewrite the same steps everywhere
* Recalculate logic every time manually

This is where **functions** come in.

Think of a function as:
A named set of instructions that does one specific job.

That’s it.

Nothing fancy.

---

What a Function Really Is (First Principles)

A function is:

* A box
* That contains steps
* That you can run whenever you want
* Without rewriting the steps again

In real life:
You don’t explain how to brush teeth every morning.
You just say: “Brush teeth”.

Your brain already knows the steps.

That shortcut is a function.

---

Why Functions Exist

Without functions:

* You repeat the same logic
* Code becomes longer
* Mistakes increase
* Fixing one bug requires fixing it everywhere

With functions:

* You write logic once
* You reuse it
* You think at a higher level

Functions reduce mental load.

---

Function vs Action (Important Difference)

Action:

* Something that happens right now
* Example: Clicking a button

Function:

* A stored set of instructions
* Example: What should happen when the button is clicked

A function does nothing by itself.
It only runs when called.

---

Writing vs Calling a Function

Writing a function:

* You are defining the steps
* Nothing executes yet

Calling a function:

* You are telling it to run now
* The steps actually execute

This separation is critical.

Many beginners get confused here.

---

Inputs and Outputs (Plain Thinking)

Some functions:

* Need information to work (input)
* Give back a result (output)

Example in real life:

* Input: Dirty clothes
* Function: Washing machine
* Output: Clean clothes

Not all functions need inputs.
Not all functions give outputs.

But thinking this way makes logic clean.

---

Functions Do NOT Remember State Automatically

Important rule:
A function does NOT remember past values by default.

Every time it runs:

* It starts fresh
* Unless state is stored somewhere else

This prevents hidden bugs.

State and functions are separate ideas.

---

Why Functions Matter in JavaScript

Everything in JavaScript relies on functions:

* Button clicks
* Counters
* Calculations
* API calls
* Animations
* Apps
* Websites

If you understand functions:
You can build real things.

Counters are just the starting point.

---

Practice Tasks (Do NOT Skip)

Task 1
In plain words, explain what a function is.

- Functions are set of instructions that performs something specific when called.

Task 2
Why is repeating the same logic multiple times a bad idea?

- It makes the code longer, non readable, slow.

Task 3
Give a real-life example of a function.
Identify its name and what it does.

- function cookMaggi
Input - Maggi noodles, water, masala
Process - Boil the noodles, masal and water on burner for 5 minutes.
Output - Maggi

Task 4
Explain the difference between writing a function and calling a function.

- Writing a function includes its name, set of instructions and the output.
- Calling a function is making it run.

Task 5
Does a function automatically remember past values?
Explain why or why not.

- Function doesnt automatically remembers past values, because each call behaves independently, unless state is tored somewhere.

Task 6
Why are functions important when building large applications?

- Function are important in builduing large applications, because they can be called again and again with different arguments.
- It also gives structure to code.

Task 7
Identify the function, input, and output in calculating the total price of items in a shopping cart.

- Function: calculateTotalPrice
- Input: list of items (price and quantity)
- Output: final total price of the cart

Task 8
Why is naming a function properly important for humans reading code?

- So that humans can understand what is the role of the function.

Task 9
What happens if a function is written but never called?

- It never runs.

Task 10
Give one real-life example where using a function reduces mental effort.

- Making tea in the morning.

---

When you finish this, type **8**.
Next chapter will connect **functions + state + loops** into actual JavaScript logic.
