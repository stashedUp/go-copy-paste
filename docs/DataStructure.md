# Data Structure

# Array
For array code comments
```
arr := [1,]
```
```
resArr := make([]int,len(arr))
```

# Map
For maps code comments
```
MapName
Key : Value
1   : 2
1   : 2
1   : 2
1   : 2
```
Map declaration
```
hashMap := make(map[int]int)
```
# Stacks
Illustrate
```
/*
stacks
| |
| |
| |
|_|

Front - Last (LIFO)

```
### Stack-Int
```go
type Stack struct {
	stack []int
}

func (this *Stack) init() {
	this.stack = []int{}
}

func (this *Stack) Peek() int {
	return this.stack[len(this.stack)-1]
}

func (this *Stack) Pop() {
	if len(this.stack) > 0 {
		this.stack = this.stack[:len(this.stack)-1]
	}
}

func (this *Stack) Top() int {
	top := this.stack[len(this.stack)-1]
	this.stack = this.stack[:len(this.stack)-1]
	return top
}

func (this *Stack) Empty() bool {
	return len(this.stack) == 0
}

func (this *Stack) Push(a int) {
	this.stack = append(this.stack, a)
}

func (this *Stack) Len() int {
	return len(this.stack) 
}
```
