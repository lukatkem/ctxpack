# Packing quality guarantees

1. Budget never exceeded — used_chars <= usable() for every algorithm
2. Named drops — every excluded document carries a named reason
3. Determinism — same docs, same budget, same packing; ties break by id
