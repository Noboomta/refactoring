# refactoring
# Refactoring Examples
# Code Chef

From CodeChef repository code: https://github.com/hhhrrrttt222111/CodeChef

In the https://github.com/hhhrrrttt222111/CodeChef/blob/main/Easy/Another%20Card%20Game%20Problem%20(CRDGAME3)/card.py

consider this code (This is my commit at last week)
```python
    for i in range(round):
        a, b, *rest = [int(e) for e in input().split()]
        n1 = a//9
        n2 = b//9
        if(n1<n2):
            output.append(f"0 {count_num(a)}")
        else:
            output.append(f"1 {count_num(b)}")
```

- Refactoring signs.
  - variable name is not understandable.
  - can less the code by insert a condition into an if condition instead of creating a new variable.
  
```python
    for i in range(round):
        num1, num2, *rest = [int(e) for e in input().split()]
        if(num1//9 < num2//9):
            output.append(f"0 {count_num(num1)}")
        else:
            output.append(f"1 {count_num(num2)}")
```