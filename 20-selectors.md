# 🧠 Chapter 20 – Selectors (Rebuilding Shape from Flat State)

Normalization flattens everything.

But UI doesn’t want flat data.

UI wants:

* A video with its comments
* A user with their posts
* A post with like count

So how do we give UI nested-looking data without actually nesting state?

Answer:

Selectors.

---

## What Is a Selector?

A selector is:

> A function that reads flat state and reconstructs the data shape needed by the UI.

It does not store data.
It does not mutate data.
It derives a view of data.

---

## Example Normalized State

```
state = {
  videos: {
    1: { id: 1, title: "React Guide", commentIds: [10, 11] }
  },

  comments: {
    10: { id: 10, text: "Nice", userId: 5 },
    11: { id: 11, text: "Helpful", userId: 6 }
  },

  users: {
    5: { id: 5, name: "Aditya" },
    6: { id: 6, name: "Riya" }
  }
}
```

Flat. Clean. Structured.

---

## UI Needs This Shape:

```
Video {
  title
  comments: [
    {
      text
      user: { name }
    }
  ]
}
```

That’s nested.

But we never store it that way.

We generate it when needed.

---

## Selector Example (Conceptually)

Selector logic:

1. Get video by ID
2. Map through commentIds
3. For each comment:

   * Get comment
   * Get user
   * Combine them
4. Return reconstructed object

The state stays flat.

The UI gets structure.

---

## Why Selectors Are Powerful

1. No duplicated state
2. No derived state stored
3. No synchronization issues
4. Controlled data flow
5. Pure functions

Selectors are safe derivation.

---

## Important Rule

Selectors compute data.

They never store it.

If you store what a selector computes,
you reintroduce derived state bugs.

---

## Deeper Insight

Normalization + Selectors = Scalable architecture.

Without selectors,
flat state becomes annoying.

With selectors,
you get best of both worlds:

* Shallow updates
* Deep UI structures

---

# Practice Tasks (Logic Only)

### Task 1

What is a selector in one sentence?

--- Selector is a function that reads flat state and reconstructs the data needed by UI.

### Task 2

Why do we need selectors in normalized state?

--- Because UI needs nested state, not flat state, selectors help in converting normalized state into nested state.

### Task 3

Why should selectors not store data?

--- Because storing derived output reintroduces synchonization issues and duplication.

### Task 4

How do selectors prevent derived state bugs?

--- Because selectors dont store data, they every time compute data from single source of truth,
    they are functions that take flat state as argument.

### Task 5

Why are selectors considered pure functions?

--- Because they take flat state as input, and returns nested state, can be called anytime.

### Task 6

Does selector output need to be stored in state? Why?

--- It doesnt need to be stored in state because it is a derived value, not a fact.

### Task 7

If a comment changes, does the video need to be replaced in state?

--- If it is a flat state, no.

### Task 8

Why do selectors improve scalability?

--- Selectors improve scalability because they decouple data storage from data presentation. 
    This allows storage to remain optimized and predictable while UI structures evolve independently.

### Task 9

What is the relationship between normalization and selectors?

--- Selectors convert normalized state data into deep layers of nested data.

### Task 10

What architectural pattern is forming from Chapters 18–20?

--- I am learning state architecture, 
    Single source of truth - Normalized states - Pure Selectors - Scalabale states 

