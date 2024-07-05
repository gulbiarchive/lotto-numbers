# lotto-numbers
🔢 Program to automatically generate lotto numbers using Python!

## random 
- 숫자를 무작위로 선택하기 위한 라이브러리

## sample()
- 주어진 시퀀스에서 중복되지 않는 임의의 샘플 선택
- 형식 : `random.sample(population, k)`
- `population` :  샘플을 추출할 대상
- `k` : 추출할 샘플의 개수
- 결론 : `population`에서 무작위로 선택된 `k`개의 요소를 포함한 새로운 리스트 반환

## 숫자 6개 조합 5세트 만들기
로또 한 장을 구매하면 다섯 게임에 참가할 수 있다.  
그러므로 6개의 숫자 조합 5개 세트를 한 번에 생성할 것이다.

- 숫자 조합 리스트를 5번 작성하는 것은 가독성도 떨어지고 중복되는 코드가 많으므로 좋지 않은 코드이다.
- 반복문을 활용하여 작성
```
import random

numbers = list(range(1, 46))

for i in range(1, 6):
    selected_numbers = random.sample(numbers, 6)
    selected_numbers.sort()
    print(f'{i}번 째 게임: {selected_numbers}')
```
