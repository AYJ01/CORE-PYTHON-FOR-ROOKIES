# Concurrency Practical Questions

1. Explain the difference between concurrency and parallelism.
2. Create a thread pool.
3. Submit tasks to a thread pool.
4. Map work over a collection.
5. Create a process pool.
6. Protect a process entry point.
7. Define an asynchronous coroutine.
8. Run coroutines with `asyncio.run()`.
9. Create tasks with `asyncio.create_task()`.
10. Wait for tasks with `asyncio.gather()`.
11. Explain cooperative multitasking.
12. Identify a blocking call in async code.
13. Protect shared state with a lock.
14. Use a queue to share work.
15. Explain what a race condition is.
16. Explain a deadlock.
17. Choose threads for I/O-bound work.
18. Choose processes for CPU-bound work.
19. Limit concurrent network requests.
20. Add cancellation handling.

## Mini-project

Build a concurrent URL checker that limits request concurrency, collects successes and failures, and reports a summary. Support a threaded implementation and a separate `asyncio` implementation.
