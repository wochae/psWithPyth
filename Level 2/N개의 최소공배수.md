wochae
```java
class Solution{
    public long gcd(long a,long b){
        if(a>b)
            return (a%b==0)? b:gcd(b,a%b);
        else
            return (b%a==0)? a:gcd(a,b%a);
    }

    public int solution(int[] arr) {
        long answer = arr[0];

        for(int i = 1;i<arr.length;i++){
            long gcd = gcd(answer,arr[i]);
            answer = answer * arr[i] / gcd;
        }
        return (int)answer;
    }
}
```
nheo
```py
// code
```
donghyuk
```py
// code
```
hakim
```py
def gcd(a, b):
    if a % b == 0:
        return b
    return gcd(b, a % b)

def solution(arr):
    if len(arr) == 1:
        return arr[0]
    answer = (arr[0] * arr[1]) / gcd(arr[0], arr[1])
    if len(arr) == 2:
        return answer
    i = 2
    while True:
        answer = (answer * arr[i]) / gcd(answer, arr[i])
        i += 1
        if i == len(arr):
            break
    return answer
```
