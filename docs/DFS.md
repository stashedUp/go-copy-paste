# DFS

```go
var stack []Node
	stack = append(stack, Node{"", 0})
	seen := make(map[Node]bool)

	for len(stack) > 0 {
		size := len(stack)
		top := stack[len(stack)-1]
		stack = stack[:len(stack)-1]

		if seen[top] {
			continue
		}

		seen[top] = true

		Printer(top) //do stuff

		for i := 0; i < size; i++ {

			for _, val := range graph[top] {
				if !seen[val] {
					stack = append(stack, val)
				}
			}
		}

	}
```