---
title: "Concurrency vs Parallelism vs Multithreading"
date: 2025-07-22 10:00:00 +0700
categories: [Computer Science, Programming]
tags: [concurrency, parallelism, multithreading, programming]
pin: true
toc: true
---

Understanding the differences between **Concurrency**, **Parallelism**, and **Multithreading** is essential for writing efficient software, especially in today’s world of multicore processors and distributed systems.

---

## 🧩 Definitions

### Concurrency
> **Concurrency** is when two or more tasks are in progress at the same time — conceptually.

- It does **not** necessarily mean they are running at the exact same time.
- Think of it like a single CPU **interleaving** execution between tasks.
- Useful in scenarios where tasks spend time waiting (e.g., I/O-bound).

📌 Example: An operating system switching between multiple processes.

---

### Parallelism
> **Parallelism** is when two or more tasks are executed **simultaneously** — literally at the same time.

- Requires **multiple cores or processors**.
- Mainly used for **CPU-bound** tasks that can be split into independent sub-tasks.

📌 Example: Matrix multiplication across multiple cores.

---

### Multithreading
> **Multithreading** is a programming technique where a single process spawns **multiple threads** to perform tasks.

- Threads **share memory space**, unlike processes.
- Can be **concurrent**, and on multi-core CPUs, also **parallel**.
- Often used to handle I/O operations or UI + background task separation.

📌 Example: A web server using threads to handle each client request.

---

## 🔄 Key Differences

| Concept        | Simultaneous? | Needs Multi-core? | Use Case         |
|----------------|----------------|-------------------|------------------|
| Concurrency    | Not necessarily| No                | I/O-bound apps   |
| Parallelism    | Yes            | Yes               | CPU-bound apps   |
| Multithreading | Maybe          | No (Yes for parallel) | UI, async tasks |

---

## 💡 Visualization

- **Concurrency**: You have one waiter juggling 5 tables (switching back and forth).
- **Parallelism**: You have 5 waiters serving 5 tables at the same time.
- **Multithreading**: One chef has 3 arms (threads), prepping salad, soup, and dessert at once.

---
