## 15 – Objects as State (Structured State)

So far you’ve learned:

* Single values as state
* Lists as state

Now we answer this question:

**What if one “item” itself has many related pieces of information?**

That’s where objects come in.

---

### The Core Truth

An object is:

> One state that groups **different but related values**

It represents **one thing**, not many things.

---

### Why Objects Exist

From first principles:

Sometimes a thing cannot be described by one value.

Example:
A user is not just a name.

A user has:

* Name
* Age
* Email
* Status

All of these belong to **one identity**.

So instead of many separate states, we group them.

---

### Object vs List (Important Distinction)

* A **list** groups many similar things
* An **object** groups many different properties of one thing

Both are just **state containers**, but with different intent.

---

### Object as One State

Very important idea:

Even though an object has many properties,
**the object itself is one state**.

You don’t treat each property as separate global state.

Why?

* They belong together
* They change together logically
* Splitting them causes sync bugs

---

### Example (Logic Only)

State:

* user

Properties inside:

* name
* loggedIn
* role

These properties are not independent states.
They are **parts of one truth**.

---

### Updating Object State (First Principles)

Logic:

1. Read the current object
2. Create a new object
3. Change only the needed property
4. Keep all others the same
5. Replace the old object

Same pattern as lists.
Same reason.
Same safety.

---

### Why Partial Updates Are Dangerous

If you update properties independently:

* One property updates
* Others stay stale
* Object becomes inconsistent

Objects represent **cohesive reality**.
They must stay consistent.

---

### Objects + Derived State

Just like lists:

* You don’t store conclusions inside objects
* You store facts

Example:

* Store `age`
* Derive `isAdult`

Never store both.

---

### Objects Inside Lists (Real Apps)

Real apps use:

* Lists of objects

Example:

* Cart → list of product objects
* Chat → list of message objects
* Users → list of user objects

This is not complex if:

* You understand lists
* You understand objects
* You update by replacement

---

### Mental Model (Very Important)

* Object = one thing
* Properties = facts about that thing
* List = many things
* State updates = replacement, not mutation

This mental model scales forever.

---

## Practice Tasks (Do NOT Skip)

Task 1
Explain what an object is, using logic words only.

- An object is a list of many properties realted to one thing.

Task 2
Give three real-world examples where object state is needed.

- Students in a class - Name, age, rollno etc.
- Cars of a brand - Name, launchyear, Price etc
- Phones of a brand - Name, Price etc.
  
Task 3
Explain why object properties should be grouped into one state.

- Becuase they are related to one thing, it makes sync and updates easier and in flow.

Task 4
Describe the logic of updating one property in an object.

- Take the object.
- Update the property.
- Replace the old object state with new object state.

Task 5
Explain why directly changing object properties can cause bugs.

- System may fail to detect the update which can cause two truths, silently bugs will appear.

Task 6
Describe how derived state works with objects.

- isAdult is a derived state, derived from students state.

Task 7
Explain the difference between a list of values and a list of objects.

- List of values has multiple values of one thing.
- List of objects has multiple properties of one related thing.

Task 8
Describe a real-world system that uses objects inside lists.

- Data of students in a school.

Task 9
Explain why replacement is safer than mutation for objects.

- Replacement is safer because it returns the new object list, which updates the whole state
  inturn not causing any bugs.

Task 10
Explain how understanding objects completes your state foundation.

- Using objects multiple properties of a thing can be stored in a state, which improves
  Overall code
  Doesn't cause bugs
  System syncs properly.

---
