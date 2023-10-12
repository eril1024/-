# H-Index
> https://school.programmers.co.kr/learn/courses/30/lessons/42747
- 사용언어 : JAVA

## 문제풀이
1. 1 부터 citation.length까지의 수에서 각 수마다 논문의 수를 비교한다.
2. 논문의 수가 i보다 이상일 경우 answer에 답을 넣고
3. answer은 최댓값이 되어야하기 때문에 최댓값을 구한다.

## Code
```
class Solution {
    public int solution(int[] citations) {
        int answer = 0;
        for(int i = 1; i<=citations.length; i++){
            int hiCnt = 0;
            for(int j = 0; j<citations.length; j++){
                if(citations[j] >= i){
                    hiCnt++;
                }
            }
            if(hiCnt >= i){
                answer = Math.max(answer, i);
            }
        }
        return answer;
    }
}
```
