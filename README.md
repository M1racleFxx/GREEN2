# ДЗ 2
## Задание 1
### Скобки
```
def check_parentheses(s):
    brackets = {
        '(': ')',
        '{': '}',
        '[': ']'
    }
    stack = []
    for char in s:
        if char in brackets:
            stack.append(char)
        elif char in brackets.values():
            if not stack or brackets[stack.pop()] != char:
                return False

    return len(stack) == 0
print(check_parentheses("(({[]}))"))
print(check_parentheses("{(})"))
print(check_parentheses('([])[[]]'))
print(check_parentheses(")())[[]]"))
print(check_parentheses("(())[[]]"))
print(check_parentheses('([])'))
```
## Задание 2
```
first_list = [1, 3, 5, 7]
second_list = [2, 4, 6, 8]

deque = (first_list + second_list)
deque.sort()
print(deque)
```
