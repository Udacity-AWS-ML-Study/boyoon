### 패키지 폴더의 구조
```bash
-distributions/
  -Gaussiandistribution.py
  -Generaldistribution.py
  -__init__.py
-setup.py
```

### 다른 파이썬 스크립트를 import할 때
```python
from .Generaldistribution import Distribution
```
* .을 import하는 파일이름 앞에 씀: Python3부터 필요해짐.
* \_\_init__.py : 이 폴더가 패키지라는 것을 알려줌
  init 파일 안에 
  ```python
  from .Gaussiandistribution import Gaussian
  ```
  이라고 넣어주면, 다른 파일에서 Gaussian 클래스를 import할 때, 그 클래스가 있는 정확한 위치까지 안 써도 되고, from distribution import Gaussian으로 사용 가능함.
  
### setup.py 
: 패키지 이름, 버전, description 등이 있음
```python
from setuptools import setup

setup(name="distributions',
      version='0.1'
      description='Gaussian distributions',
      package=['distributions'],
      zip_safe=False)
      
```

이렇게 setup.py 파일과 distributions 폴더(본인이 패키지로 만들고 싶은 폴더)가 완성된 후, 
```python
pip install .
```
실행하면 자동으로 setup.py 을 찾아서 python package를 설치함

이제 로컬에서 distributions 패키지를 사용할 수 있다!

패키지가 어디에 설치되었는지 확인하려면
```python
import distributions

distributions.__file__
```

local에서 패키지 설치해서 사용하려면 가상환경을 설치해서 쓰는 것이 좋음

---
실습했을 때 만난 문제들
1. matplotlib 등이 자동으로 안 깔렸음.


