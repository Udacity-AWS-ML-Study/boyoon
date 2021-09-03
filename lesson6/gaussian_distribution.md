## Normal distribution(Gaussian distribution)

* sample std

By default, numpy.std returns the population standard deviation, in which case np.std([0,1]) is correctly reported to be 0.5. If you are looking for the sample standard deviation, you can supply an optional ddof parameter to std():
```python
np.std([0, 1], ddof=1)
https://stackoverflow.com/questions/34050491/standard-deviation-in-numpy
```
* population std

넘파이의 std의 기본 설정
```python
np.std([0, 1], ddof=1)
```
