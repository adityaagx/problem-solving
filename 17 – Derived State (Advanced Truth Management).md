# 🧠 17 – Derived State (Advanced Truth Management)

So far you’ve learned how to **store truth safely**.

Now we answer this question:

> Should we store everything we need inside state?

The answer is:

> No.

And this chapter explains why.

---

# The Core Truth

Derived state is:

> A value that can be calculated from existing state.

If something can be calculated,
it should not be stored.

---

# Why This Matters

State represents **source of truth**.

If you store both:

* The facts
* And conclusions derived from those facts

You now have:

Two sources of truth.

And two sources of truth eventually disagree.

That’s when bugs appear.

---

# First Principles Example

You store:

* age = 20
* isAdult = true

What happens if age becomes 17,
but isAdult is not updated?

Contradiction.

The system now believes two conflicting realities.

That’s state corruption.

---

# The Rule of Derived State

> Store facts.
> Derive conclusions.

Never store both.

---

# Examples of Derived State

If you have a list of cart items:

Each item:

* price
* quantity

You should store:

* price
* quantity

You should NOT store:

* totalPrice

Because totalPrice can be calculated.

If you store totalPrice separately,
it can go out of sync.

---

# Derived State With Lists of Objects

Suppose:

students = [
{ name: "A", score: 80 },
{ name: "B", score: 90 }
]

You want:

* classAverage

Do you store classAverage inside state?

No.

Because it can be calculated from scores.

If you store it,
you must update it every time a student changes.

That’s fragile.

---

# Why Beginners Store Derived State

Because it feels convenient.

They think:

> “I already calculated it. I’ll just store it.”

But that creates maintenance burden.

Now every update must:

* Update facts
* Update conclusions

One missed update → bug.

---

# The Deep Principle

State should represent:

> The minimal information required to reconstruct reality.

Nothing more.

Nothing duplicated.

---

# Signs You Are Storing Derived State

You might be storing derived state if:

* You store counts of items in a list.
* You store totals.
* You store filtered lists.
* You store flags based on other values.
* You store status that can be computed.

If something depends entirely on other state —
it is derived.

---

# When Derived State Is OK To Store (Rare)

There are only two valid reasons:

1. Performance (expensive calculation)
2. External synchronization requirements

But even then:
You must manage it carefully.

Default rule:
Do not store it.

---

# Mental Model Upgrade

Before Chapter 17:
State = container of data.

After Chapter 17:
State = minimal atomic truth.

Everything else = projection.

That’s a massive shift.

---

# Practice Tasks (Do NOT Skip)

### Task 1

Explain what derived state is using pure logic words.

--- Derived value is the state derived from other states values.

### Task 2

Why does storing derived state create two sources of truth?

--- Because if one changes and the other doesnt, it now causes contradiction.

### Task 3

Give three examples of derived state in real-world systems.

--- Average age of students in a class
--- Average marks of students in a class
--- Total no of marks of a student in every subject.

### Task 4

In a cart system, explain why storing totalPrice can cause bugs.

--- If new items are added or removed, totalPrice may fail to update, causing bugs.

### Task 5

Explain the difference between a fact and a conclusion in state design.

--- A fact is a single store of truth 
--- A conclusion is a state derived from other state or fact.

### Task 6

If you store:

* firstName
* lastName
* fullName

Which one is derived? Why?

--- fullName is a derived state, because it derives its value from firstName and lastName.

### Task 7

In a list of todos, is “completedCount” derived? Explain.

--- Yes, completedCount is derived because it shows the total no of counts completed, 
    which cant remain the same, and has to be calculated each time.

### Task 8

Describe a bug scenario caused by storing derived state.

--- If totalPrice in a cart is stored as a derived state, it will not update automatically
    when items are changed in a cart, causing bugs in system.

### Task 9

Explain why minimal state scales better in large systems.

--- Because single source of truth remains minimal, everything else will be derived from these only,
    causing less bugs and easy update management.

### Task 10

How does understanding derived state change how you design apps?

--- Derived state is very crucial in understanding large scalable systems because now i understand,
    why state facts should be minimal, and derived state always easily updates.

This chapter is subtle.

If Chapter 16 prevents mutation bugs,
Chapter 17 prevents logic contradictions.

Answer slowly.

This is how senior engineers think.
