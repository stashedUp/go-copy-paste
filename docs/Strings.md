# Strings

## String Builder
```go
func join(strs ...string) string {
	var sb strings.Builder
	for _, str := range strs {
		sb.WriteString(str)
	}
	return sb.String()
}
```
```
var sb strings.Builder
```
```
sb.WriteString(str)
```
```
return sb.String()
```
## Contains
Returns boolean
```
strings.Contains("warren code", "code")
```
## Fields
String s is split on the basis of white spaces and store in a string array
```
v = strings.Fields("warren code")
```
## Repeats
Repeats string 4 times
```
res := strings.Repeat(str1, 4)
```
## ReplaceAll
Returns new string with replaced word. Can be used to replace white character
```
strings.ReplaceAll("original string to replace", "replace", "new")
```
## Index
Index returns the index of the first instance of substr in s, or -1 if substr is not present in s
```
strings.Index("chicken", "ken")
```
Return 4. 
str := "chicken"

idx := strings.Index(str, "ken")

fmt.Print(str[:idx])


