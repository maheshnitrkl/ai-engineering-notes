# Quiz Review

Based on the actual quiz from Phase 0, Lesson 05 (Jupyter Notebooks).

## Question 1 (Pre)
**What is a Jupyter notebook?**

> **Correct answer:** An interactive document that mixes executable code cells with markdown text and inline outputs.

A Jupyter notebook (`.ipynb`) lets you write and execute code in cells, see outputs inline, and mix code with formatted text explanations.

---

## Question 2 (Pre)
**What does the Jupyter kernel do?**

> **Correct answer:** Runs the code in cells and keeps variables in memory between executions.

The kernel is a separate Python process. All cells share the same kernel, so a variable defined in one cell is available in all subsequent cells.

---

## Question 3 (Post)
**What is the difference between `%timeit` and `%%time`?**

> **Correct answer:** `%timeit` runs code many times and averages; `%%time` runs code once.

- `%timeit` → statistical average (good for microbenchmarks, small fast operations)
- `%%time` → single run, wall time (good for training runs, longer operations)

---

## Question 4 (Post)
**What is the most common cause of a notebook working on your machine but failing when someone runs it top to bottom?**

> **Correct answer:** Out-of-order cell execution creating hidden dependencies on execution order.

If you run cells out of order, variables may exist because you ran cell 5 before cell 2. The fix is **Kernel > Restart & Run All** to verify linear execution.

---

## Question 5 (Post)
**When should you move code from a notebook into a `.py` script?**

> **Correct answer:** When the code is a reusable utility, training pipeline, or production code.

The rule is **"explore in notebooks, ship in scripts."** Notebooks are for exploration and prototyping; `.py` files are for reusable, schedulable, production code.

---

**Study tip:** If you can explain each of these five answers in your own words, you understand the core concepts of this lesson.
