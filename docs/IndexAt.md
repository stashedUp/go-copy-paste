go# IndexAt - used to find the index at a slice

```go
func indexOf(arr []int, val int) int {
    for pos, v := range arr {
        if v == val {
            return pos
        }
    }
    return -1
}
```
