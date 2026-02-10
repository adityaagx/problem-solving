## 13 – Derived State (State That Comes From Other State)

This chapter answers one deep question:

**Should everything be stored as state?**

The answer is **no**.

Some things should be **calculated**, not remembered.

---

### The Core Truth

State is memory.

But:

> Memory should store only what you cannot easily recalculate.

If you store too much:

* Memory contradicts itself
* Bugs appear
* Logic becomes fragile

So we introduce **derived state**.

---

### What Is Derived State?

From first principles:

Derived state is:

* A value that is not stored directly
* But calculated from other state
* Whenever needed

It represents **logic**, not memory.

---

### Simple Example (Logic Only)

State:

* number of items
* price per item

Derived:

* total price

Important:

* Total price is not independent
* It depends entirely on other values
* Storing it creates duplication

---

### Why Duplication Is Dangerous

If you store:

* item count
* total price

You now have **two sources of truth**.

If one updates and the other doesn’t:

* The system lies
* UI shows wrong information
* Bugs appear silently

This is one of the most common real-world mistakes.

---

### The Golden Rule

**Never store what can be derived.**

Store:

* Facts
* Inputs
* Independent values

Derive:

* Totals
* Status messages
* Conditions
* Labels

---

### Memory vs Logic

State = memory
Derived state = logic

Memory:

* Needs updates
* Can become outdated

Logic:

* Always correct
* Always fresh
* Depends on current state

Good systems rely more on logic than memory.

---

### Example: Status Message

State:

* count

Derived:

* message (“Low”, “Normal”, “High”)

The message should not be stored.
It should be **decided**.

If count changes:

* Message automatically stays correct
* No extra updates needed

---

### Why Beginners Get This Wrong

Because storing feels easier.

But:

* Easy now = painful later
* More state = more bugs
* Less state = more clarity

Professional systems minimize stored state.

---

### Derived State Still Feels Like State (But Isn’t)

It looks like state.
It behaves like state.
But it has **no memory**.

It is recreated every time from truth.

That’s why it’s safe.

---

### Mental Test (Use This Forever)

Before creating a new state, ask:

> “Can this be calculated from existing state?”

If yes:

* Do not store it

If no:

* It deserves to be state

This one question prevents huge messes.

---

### Why This Chapter Changes Everything

After this:

* Your apps feel simpler
* You stop syncing values manually
* You trust logic over memory

This is the mindset frameworks expect.

---

## Practice Tasks (Do NOT Skip)

Task 1
Explain the difference between stored state and derived state.

- Stored state is the current value which is stored.
- Derived state is the state which is derived from other states through logic.

Task 2
Give an example of something that should be derived, not stored.

- Total price of items in cart should always be derived not stored.

Task 3
Explain why storing derived values causes bugs.

- Storing derived values causes bugs, because they can change at any point in time
  and the states affecting it also change, if both change, state becomes confused, bugs appear.

Task 4
Describe a situation where two stored states can contradict each other.

- itemsInCart - 3
- TotalPrice - 150
  itemsInCart updates to 2, totalPrice still remains same, hence contradiction.

Task 5
Explain why derived state is always up-to-date.

- Derived state is always derived from up to date incoming data from other states, hence.

Task 6
Describe how a message can be derived from a numeric state.

- If numeric state < 10 -- Low
     numeric state > 10 -- High

Task 7
Explain why fewer stored states make systems safer.

- Systems will have fewer memory and more logic.
- States doesn't have to be synced manually.

Task 8
Describe a real-world example of deriving instead of remembering.

- Bank balance state is derived from transactions state.

Task 9
Explain how derived state reduces mental load.

- System works on logic not memory.

Task 10
Explain why this chapter is critical before learning arrays.

- This chapter explains derived states, which scales logic cleanly, which will be helpful in learning arrays.

---
