test PyPi 에 테스트로 올려놓고 좀 안정화되면 PyPi에 올리는 것을 추천함

1. 패키지 구성
```bash
package/license.txt
package/python_scripts.py
package/README.md : 패키지 소개
package/setup.cfg : README
setup.py
```

예시
```python
setup(name= "package_name",
      version = '1.1',
      description = "package discription",
      packages=['package_name"],
      author = "your name",
      author_email = "youremail@dd.com",
      zip_safe=False) #zipfile 상태에서 실행할 수 있는지
```
2. 실행
```bash
$ python setup.py sdist
```

3. dist 폴더 안에 tar.gz 파일 생김
4. pip install twine
5. Pypi에 패키지 업로드

```bash
$ twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```
유저이름과 비밀번호 
