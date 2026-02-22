05 - Conditions (Decision Making)

Goal of this lesson
To understand how programs make decisions.
This is where logic becomes powerful and real applications begin.

First principle: programs do not “decide” naturally

A program does not think.
It does not judge.
It does not understand meaning.

It only follows rules.

If this is true, do this.
If not, do something else.

This rule-based decision making is called a condition.

---

What a condition really is

A condition is a question with only two possible answers:
Yes or No
True or False

There is no maybe.

Examples:
Is the light on?
Is the count greater than 5?
Is the user logged in?
Is the cart empty?

Each question results in either true or false.

---

First principle: conditions depend on state

A condition does not exist alone.
It always checks state.

Condition = a question about the current state.

If there is no state, there is nothing to check.

Example:
State: count = 3
Condition: is count greater than 2?
Answer: yes

---

Real-life example: door lock

State: door is locked

Condition:
Is the door locked?

If yes → unlock it
If no → do nothing

The program is not smart.
It is just following rules.

---

Very important rule

Conditions do not change state.
They only choose what action happens next.

Actions change state.
Conditions choose actions.

This distinction matters a LOT.

---

Example: volume control

State: volume = 10

Condition:
Is volume greater than 0?

If yes → allow volume down
If no → do nothing

The condition did not change volume.
It only allowed or blocked an action.

---

First principle: every decision is branching

When a condition is checked, the program chooses a path.

Path 1: condition is true
Path 2: condition is false

This is called branching.

Programs are basically a collection of branches.

---

Example: login system

State: userLoggedIn = false

Condition:
Is user logged in?

If yes → show dashboard
If no → show login screen

Same app.
Different path.

---

First principle: order matters

Conditions are checked in order.

Once a condition matches, the program follows that path.

Wrong order = wrong behavior.

This is why logic bugs happen.

---

Common beginner mistakes

Thinking conditions change values
Forgetting what state is being checked
Checking the wrong state
Assuming the program “knows” intention
Using vague conditions instead of exact ones

Conditions must be precise.

---

Golden thinking pattern (memorize this)

Check state
Decide path
Perform action
Update state

This loop runs constantly in real apps.

---

Practice Tasks (Do NOT Skip)

Task 1
Identify the condition when turning a fan off if it is already running.

- If fan is on, press the switch downwards.

Task 2
What condition must be checked before increasing a counter beyond 10?

- If counter is less than 10, allow increase, else no.

Task 3
Describe a condition used before sending a message on WhatsApp.

- If mobile data is on, send the message, else block.

Task 4
What condition decides whether a user sees a login screen or dashboard?

- If user is logged in a dashboard is shown, else login screen is shown.

Task 5
Identify the condition used to prevent volume from going below zero.

- If volume is zero, only volume up button works.

Task 6
Explain a condition used when adding an item to a cart only if it is in stock.

- If a item is in stock, Add to cart option is shown, else, Out of stock is shown.

Task 7
What condition is checked before deleting a file?

- If a file is present it can be deleted, else no.

Task 8
Identify the condition that decides whether a “Like” button increases the count.

- Has the user already liked, if yes, unlike it and decrease the count by one, else increase the count by one

Task 9
Explain why conditions alone cannot change state.

- Conditions are just instructions which tell the program as to what to do when something happens
  thereby resulting in actions, which thereby change state.

Task 10
Give one real-life example of a condition and the action it allows or blocks.

- Did a pushup occur, if yes increase the count by one, else do nothing.

Lesson 05 takeaway

Conditions ask questions.
State provides answers.
Actions do the work.
Together, they create logic.
