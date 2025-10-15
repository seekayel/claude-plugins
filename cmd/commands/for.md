---
description: Loop over the template provided using for loop style syntax and add each to todo list with TodoWrite
---

# For (loop) Command

Use the for loop like syntax to call `TodoWrite` on the template provided substituting the input variables.


## Examples

**Enumerated array**
```
/for i in [3,5,42] "Pull github PR ${i} a code review focusing on security concerns."
```

Will do exactly the following:
```
Call /TodoWrite on [
"Pull github PR 3 a code review focusing on security concerns.",
"Pull github PR 5 a code review focusing on security concerns.",
"Pull github PR 42 a code review focusing on security concerns."
] then confirm the plan with the user before executing
```


**Iteration**
```
/for i in range(1, 3):
Pull github PR ${i} a code review focusing on security concerns.
```

Will output:
```Call /TodoWrite on [
"Pull github PR 1 a code review focusing on security concerns.",
"Pull github PR 2 a code review focusing on security concerns.",
"Pull github PR 3 a code review focusing on security concerns."
] then confirm the plan with the user before executing
```