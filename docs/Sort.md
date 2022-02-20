# Sort Slice

Java has Array.sort(words). GO does not have a build in function. We have to do it from scratch.

### Slice words lexicographically
```go
	sort.Slice(words, func(i, j int) bool {
		return len(words[i]) < len(words[j])
	})
```
