04 - Actions and State Changes (Transitions)

Goal of this lesson
To understand how actions change state.
This is the missing link that makes counters, buttons, and logic finally click.

First principle: nothing changes unless something happens

A program does not change by itself.
State does not change automatically.
Values do not move on their own.

Something must happen.

That “something” is called an action.

Action means:
A click
A button press
Typing
Swiping
Time finishing
An event occurring

No action means no state change.

What an action really is

An action is an event that tells the program:
“Now something should change.”

Actions do not store values.
Actions only cause changes.

State stores values.
Actions modify them.

Action and state are different things.

Very important rule

Action is not state.

Action triggers change.
State holds the result.

Example: light switch

Current state: light is OFF
Action: press switch
New state: light is ON

The switch press is not the state.
The light being on or off is the state.

Example: counter button

Current state: count is 0
Action: button click
New state: count becomes 1

Button click is an action.
The number is the state.

First principle: every action causes a transition

A transition means:
State A becomes State B

Nothing more.
Nothing less.

Example:
Volume is 6
Action: press volume down
Transition: volume becomes 5

This movement from 6 to 5 is a state transition.

Thinking like a programmer

Programmers constantly ask three questions:

What is the current state?
What action just happened?
How should the state change because of that action?

If you can answer these three, you can solve the problem.

Example: pushups

Current state: count is 3
Action: one pushup completed
New state: count becomes 4

Action caused transition.

Example: shopping cart

Current state: items are 2
Action: add item
New state: items become 3

Same pattern every time.

First principle: one action can change one or many states

Sometimes an action changes one thing.
Sometimes it changes multiple things.

Example: placing an order

Action:
User clicks “Place Order”

State changes:
Cart becomes empty
Order count increases
Payment status changes
Confirmation message appears

One action causes many state changes.

First principle: state change logic must be explicit

The program will not guess.
It will not assume.
It will not understand intention.

You must define:
If this action happens,
change state like this.

No definition means no change.

Common beginner mistakes

Thinking the button stores the value
Expecting state to change automatically
Forgetting to update the state
Confusing action with result
Assuming previous values still exist

Most bugs come from these mistakes.

Golden formula (memorize this)

Current state
plus action
results in new state

Every programming problem reduces to this.

Practice Tasks (Do NOT Skip)

Task 1
Identify the action and the state change when a fan goes from speed 1 to speed 2.

- Action is pressing the button to increase speed.
- State is the resulting changed speed which is 2.

Task 2
What is the action and what is the state when a button click increases a counter?

- Action is the click of button.
- State is the resulting value of a counter

Task 3
Describe the transition when phone volume goes from 3 to 4.

- Action is the pressing of volume button.
- State is the resulting volume of phone which is 4.

Task 4
In a game, what action causes the score to change?

- Action of playing and scoring changes the score state value.

Task 5
Identify the state and action in marking a message as read.

- Action is the opening of chat which thereby results in the chat being shown read.
- State is the value which is read thereby.

Task 6
Explain what happens to state when you press refresh on a webpage.

- State loses most of the memory and initializes to its initial value.

Task 7
What action causes the shopping cart count to decrease?

- Placing the order can decrease the cart count.
- Removing the item from the cart can also decrease the count.

Task 8
Identify multiple state changes caused by logging out of an app.

- Profile state changes from loggedin to loggedout.
- Cart state changes to initial value, 0 in most cases.
- Wishlist state changes to initial value, 0 in most cases.
- Account information changes to initial value, blank in most cases.

Task 9
Why does state not change if no action happens?

- Action is needed to change the value.
- Without any action, value remains the same.

Task 10
Give one real-life example of current state, action, and new state.

- Counting pushups
- Current state is 1
- Does one more pushup.
- Value increase by one.
- State changes to 2.

Lesson 04 takeaway

Actions trigger change.
State stores values.
Transitions move state forward.
If you can track actions and state, you can think like a programmer.
