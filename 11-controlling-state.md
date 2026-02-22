11 - Controlling State (Increase, Decrease, Limits) — First Principles Only

This chapter is not about JavaScript.
It is about **control**.

You already know how to:

* Store a value (state)
* Change it using an action
* Run logic using a function

Now we ask a deeper question:

How do we **control when state is allowed to change**?

---

The Core Truth

State should **not change freely**.

If state changes without rules:

* Bugs appear
* Values break
* Systems become unpredictable

So we introduce **constraints**.

Constraints are rules that protect state.

---

What Does “Increase” Really Mean?

First principles:

Increasing means:

* Take the current value
* Replace it with a larger value

Nothing more.

It is not a button.
It is not code.
It is just **replacement of stored value**.

---

What Does “Decrease” Really Mean?

Decreasing means:

* Take the current value
* Replace it with a smaller value

Same idea.
Opposite direction.

Increase and decrease are not special operations.
They are just **controlled replacements**.

---

Why Decrease Is Dangerous

If we decrease blindly:

* Values can go below zero
* Negative state appears
* Logic breaks

So we ask:

Should this change be allowed?

This question introduces **limits**.

---

Limits (Very Important Concept)

A limit is:
A boundary beyond which state must not change.

Examples:

* Volume cannot go below 0
* Volume cannot go above max
* Counter cannot be negative
* Cart count cannot be less than zero

Limits protect state.

---

How Limits Actually Work

First principles logic:

Before changing state:

* Look at current state
* Ask: is this change allowed?

If yes:

* Change the state

If no:

* Do nothing

That’s it.

Limits do not change state.
They only **block or allow actions**.

---

Increase With a Limit (Logic Only)

State:

* count

Action:

* user presses increase

Rule:

* allow only if count is less than maximum

Effect:

* count increases only within bounds

This is control.

---

Decrease With a Limit (Logic Only)

State:

* count

Action:

* user presses decrease

Rule:

* allow only if count is greater than zero

Effect:

* count never becomes negative

Same pattern.
Different direction.

---

Why Two Buttons Are Not Special

An increase button and a decrease button are:

* Two different actions
* Acting on the same state

State is central.
Buttons are just triggers.

This is how real UIs work.

---

Why This Is Not “More Complex”

This chapter adds **no new ideas**.

It only combines:

* State
* Action
* Condition
* Function

In a stricter way.

More control ≠ more complexity.
It means better thinking.

---

Mental Checklist (Use This Forever)

Before changing any state, ask:

1. What is the current value?
2. What action is happening?
3. Should this change be allowed?
4. What is the new value if allowed?

If you can answer these, you can code it.

---

Practice Tasks (Do NOT Skip)

Task 1
Explain, in logic words, how a decrease button works.

- It takes the current value of state, and replaces it with a new smaller value.

Task 2
Why must a counter never go below zero?

- A counter count things, and counting never goes in negative.

Task 3
Describe how limits protect state.

- Limits specify the boundaries, minimum and maximum for state.

Task 4
Explain why limits do not change state by themselves.

- Limits are just boundaries, action is always needed to change state.

Task 5
Describe the logic of increasing volume with a maximum limit.

- Limit - Increase volume if the state is not maximum.

Task 6
Explain what happens when an action is blocked by a condition.

- Action happens but state is not changed if the condition blocks it.

Task 7
Describe a real-life system that uses upper and lower limits.

- Battery power in laptop, 0% <= Battery power <= 100%

Task 8
Explain why state must be checked before updating.

- State must be checked before updating, so as to check the condition if it passes.
  
Task 9
Describe how two buttons can control the same state.

- Increase button and decrease button of likes control the state of likesCount.

Task 10
Explain why this chapter gives you real control over behavior.

- It explain states and its limits & how to use them in real world logic.
---

This chapter is **pure logic discipline**.
No syntax.
No tricks.
