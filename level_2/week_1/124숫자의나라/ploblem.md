# 124 나라의 숫자

## 문제 설명

124 나라가 있습니다. 124 나라에서는 10진법이 아닌 다음과 같은 자신들만의 규칙으로 수를 표현합니다.

1. 124 나라에는 자연수만 존재합니다.
2. 124 나라에는 모든 수를 표현할 때 1, 2, 4만 사용합니다.
   예를 들어서 124 나라에서 사용하는 숫자는 다음과 같이 변환됩니다.

## 제한 조건

n은 500,000,000이하의 자연수 입니다.

## 입출력 예

| n   | return |
| --- | ------ |
| 1   | 1      |
| 2   | 2      |
| 3   | 4      |
| 4   | 11     |

## solution

```js
function solution(n) {
  var answer = "";
  var mod;
  while (n) {
    mod = n % 3;
    n = parseInt(n / 3);
    if (mod == 0) {
      n -= 1;
      answer += "4";
    } else answer += mod;
  }
  return answer.split("").reverse().join("");
}
```
