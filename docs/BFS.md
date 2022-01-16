# BFS

```go
var queue []*TreeNode

queue = append(queue, target)
var depth int
for len(queue) > 0 {
    size := len(queue)
    for i := 0; i < size; i++ {
        node := queue[0]
        queue = queue[1:]

        if depth == K {
            ans = append(ans, node.Val)
            continue
        }

        parent := data[node]

        if parent != nil && !visited[parent] {
            queue = append(queue, parent)
        }

        if node.Left != nil && !visited[node.Left] {
            queue = append(queue, node.Left)
        }

        if node.Right != nil && !visited[node.Right] {
            queue = append(queue, node.Right)
        }

        visited[node] = true
    }
    depth++
}
```