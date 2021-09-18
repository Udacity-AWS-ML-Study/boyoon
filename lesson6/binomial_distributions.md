자꾸 나는 에러
```python
self.stdev = math.sqrt(self.n * self.p * (1-self.p))
ValueError: math domain error
```
원인: math 모듈 중에 sqrt랑 log 함수 안에 인자를 0이나 음수를 넣으면 이 에러남

test.py에 음수도 없는데 왜 자꾸 에러나지?
