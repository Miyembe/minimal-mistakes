# Problems
I tried to append each list in the nested list, but I found that lists in the nested list are appended together even though I appended single list. 

# Solutions

```
x = [list()]*num_robots
x = [[] for i in range(num_robots)]
```

Both give same list shape but they work in a different manner.
