# Programmer Brain Training Roadmap (JavaScript)

State → Action → Condition → Function → Loop → State gets updated.

> Goal: Train my brain to think like a programmer so I can solve problems confidently.

---

### 1️⃣ Core Mental Model Learned

* State should **never be mutated**
* State should **always be replaced**
* Systems detect change using **reference**, not internal mutation
* Mutation causes **silent bugs**, replacement keeps system in sync

---

### 2️⃣ Single-Value State (Completed Earlier)

* State holding one value (number, string, boolean)
* Updating means:

  * Take old value
  * Create new value
  * Replace old state
* Derived state should not be stored separately

---

### 3️⃣ List (Array) State — COMPLETED

**Key concepts learned:**

* A list is a single state holding multiple related values
* Lists must be treated as **one unit**
* Adding/removing items must create a **new list**
* `push()` mutates → ❌ not safe for state
* `concat()` / spread → creates new list → ✅ safe
* List length should be **derived**, not stored
* Replacing lists is safer than modifying them
* Lists are harder than single-value state because they involve multiple values

**Practice Tasks Completed:**

* What a list is (logic-based)
* Real-world list examples
* Why lists are one state
* Adding/removing logic
* Derived state with lists
* Why mutation causes contradictions

---

### 4️⃣ Object State — COMPLETED

**Key concepts learned:**

* An object is one state grouping multiple related properties
* Properties should be grouped to stay synchronized
* Updating object state requires:

  * Copy object
  * Change one property
  * Replace entire object
    
* Direct mutation causes silent bugs
* Derived state comes from object properties (e.g., `isAdult` from `age`)
* Replacement is safer than mutation

**Practice Tasks Completed:**

* What an object is
* Real-world object examples
* Why grouping properties matters
* Object update logic
* Mutation bugs
* Lists of values vs lists of objects
* Objects inside lists (real systems)
* Why objects complete state foundation

---

### 5️⃣ VERY IMPORTANT CLARITY ACHIEVED

* `push()` vs `concat()` confusion resolved
* Mutation is allowed for **local variables**
* Mutation is **not allowed for state**
* Replacement = predictable systems
* Mutation = hidden errors

---

## Chapter 16: Lists of Objects (MOST IMPORTANT)

* Updating one object inside a list
* Adding objects to list immutably
* Removing objects from list immutably
* Updating nested properties safely
* Why this is where most beginners fail

---

## Chapter 17: Derived State (Advanced)

* Derived state vs stored state
* When NOT to store derived values
* Computing values from lists & objects
* Preventing contradictory state

---

## Chapter 18: Nested State

* Objects inside objects
* Lists inside objects
* How deep nesting causes bugs
* How to safely update nested state

---

## Chapter 19: State Normalization (Conceptual)

* Why deeply nested state is dangerous
* Flat vs nested data
* Real-world system design logic

---

## Chapter 20: State Update Patterns

* Add
* Remove
* Update
* Toggle
* Replace
  (All patterns applied to objects & lists)

---

## Chapter 21: React State Mapping (When Ready)

* Applying all logic to `useState`
* Why React behaves the way it does
* How React detects changes
* Writing bug-free React state updates

---

## Chapter 22: Mental Models of State (Expert Level)

* State as truth
* State as history
* State as source of UI
* Why immutability scales systems

---

