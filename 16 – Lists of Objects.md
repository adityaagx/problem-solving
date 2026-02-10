# 🧠 16 – Lists of Objects (Real-World State)

So far you’ve learned:

* Single values as state
* Lists as state
* Objects as state

Now we answer the next unavoidable question:

**What if I have many things, and each thing itself has many related properties?**

That’s where **lists of objects** come in.

---

## The Core Truth

A list of objects is:

> **One state that represents many things, where each thing is itself structured**

It is still **one state**.
Just more layered.

---

## Why Lists of Objects Exist

From first principles:

Real systems are not made of:

* single values
* flat lists

They are made of **entities**.

Examples:

* A school has **students**
* A shop has **products**
* An app has **users**
* A game has **players**

Each entity:

* Is one thing
* Has multiple properties
* Exists alongside other similar entities

So we need:

* A list → to hold many things
* Objects → to describe each thing

---

## List of Objects = One State

Very important clarity:

Even though it contains:

* many items
* many objects
* many properties

👉 **The entire list is still one state**

You do **not** treat:

* each object as its own global state
* each property as its own state

Why?

* The list represents one system
* Objects inside it must stay in sync
* Partial updates create contradictions

---

## Example (Logic Only)

State:

* students

Each item inside:

* id
* name
* age
* grade

These students are:

* separate entities
* but part of one system

So the **list of students** is the state.

---

## The Danger Zone (Why This Is Hard)

Lists of objects are tricky because mutation can happen at **three levels**:

1. The list itself
2. An object inside the list
3. A property inside the object

Breaking rules at **any level** breaks state safety.

This is why most bugs live here.

---

## The One Rule That Saves Everything

> You never change existing state
> You always create a new version

That applies to:

* the list
* the object
* the property

You don’t “edit”.
You **rebuild**.

---

## Updating One Object Inside a List (First Principles)

When you want to update **one item**:

Logic steps (no code):

1. Look at every item in the list
2. Identify the one that should change
3. Keep all others exactly the same
4. Create a **new object** for the changed item
5. Create a **new list** containing:

   * old objects (unchanged)
   * the new object (replaced)
6. Replace the old list

Only what changed becomes new.
Everything else stays untouched.

---

## Why Finding + Editing Is Dangerous

Common wrong instinct:

> “I’ll find the object and change one property”

Why this fails:

* Finding gives you a **reference**
* Changing it mutates existing state
* The system still sees “same object”
* Updates become invisible or inconsistent

This causes **silent bugs**, not crashes — the worst kind.

---

## What Actually Changes (Mental Model)

When updating one item:

* The list → new
* The changed object → new
* All other objects → same

Nothing else should change.

This is the **minimum safe update**.

---

## Derived State Still Applies

Same rule as before:

* Store **facts**
* Derive **conclusions**

Example:

* Store `quantity` and `price`
* Derive `totalCost`

Never store both inside objects.

---

## Real Apps Are Built On This

Almost every real app is:

* A list of objects
* Updated one item at a time
* Re-rendered based on replacement

If you understand this chapter deeply,
you understand **90% of application state**.

---

## Mental Model (Lock This In)

* List = many things
* Object = one thing
* Properties = facts about that thing
* State = one truth
* Updates = replacement, not mutation

This model scales forever.

---

## Practice Tasks (Do NOT Skip)

### Task 1

Explain what a **list of objects** is, using logic words only.

- List of objects is a state which has many objects and each object ahs many properies of related type.

### Task 2

Give three real-world examples where a list of objects is required.

- Students in a school
- Cars in a showroom
- Employees in a company

### Task 3

Explain why a list of objects is still considered **one state**.

- List of objects is still considered one state because it contains objects and properties of related type only.

### Task 4

Describe, step by step, the logic of updating **one object** inside a list (no code).

-
### Task 5

Explain why copying the list but changing an existing object inside it is still dangerous.

---

### Task 6

In a todo app with todos as objects, explain:

* What stays the same
* What becomes new
  when marking one todo as completed.

---

### Task 7

Explain how derived state works with lists of objects.

---

### Task 8

Describe a real-world system that breaks if objects inside a list are mutated directly.

---

### Task 9

Explain why lists of objects are where most beginners get bugs.

---

### Task 10

Explain how mastering this chapter changes how you think about apps.

---
