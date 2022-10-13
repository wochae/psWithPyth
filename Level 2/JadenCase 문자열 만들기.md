wochae
```py
def solution(s):
    answer = ''
    s = s.split(' ')
    for i in range(len(s)):
        s[i] = s[i].capitalize()
    answer = ' '.join(s)
    return answer
```
nheo
```py
// code
```
donghyuk
```py
import re

def to_jadencase(m):
    return m.group(0)[0].upper() + m.group(0)[1:].lower()

def solution(s):
    return re.sub("[0-9a-zA-Z]+", to_jadencase, s)
```
hakim
```py
// code
```
