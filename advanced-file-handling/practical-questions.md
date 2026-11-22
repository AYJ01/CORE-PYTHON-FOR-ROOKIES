# Advanced File Handling Practical Questions

1. Open a text file with an explicit UTF-8 encoding.
2. Replace invalid characters while reading.
3. Configure line buffering.
4. Stream a large file line by line.
5. Stream fixed-size binary chunks.
6. Create a memory-mapped file.
7. Search memory-mapped data.
8. Use `NamedTemporaryFile`.
9. Use `TemporaryDirectory`.
10. Create a ZIP archive.
11. Extract a ZIP archive safely.
12. Create a TAR.GZ archive.
13. Compress a file with gzip.
14. Stream compression for a large file.
15. Compress bytes with bzip2.
16. Use an exclusive file lock.
17. Prevent concurrent writes to a shared log.
18. Process many files recursively with `rglob()`.
19. Compare streaming and bulk loading memory use.
20. Handle corrupted or invalid archive files safely.

## Mini-project

Create a log processor that recursively finds log files, streams them line by line, extracts error records, writes a compressed report, and stores the result in a safe temporary or output directory.
