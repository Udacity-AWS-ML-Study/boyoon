super와의 차이

https://stackoverflow.com/questions/576169/understanding-python-super-with-init-methods

```python
class Blouse(Clothing):
  """inherits from Clothing class : color, size, style, price
  """
  def __init__(self, color, size, style, price, country_of_origin):
     # super().__init__() #부모 클래스의 init 전체 호출 super().__init__()
      Clothing.__init__(self, color, size, style, price) #부모 클래스의 일부 init 호출 
      self.country_of_origin = country_of_origin
```
