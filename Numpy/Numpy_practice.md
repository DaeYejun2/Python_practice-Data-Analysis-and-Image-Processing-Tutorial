# Numpy 기본 사용법

### Python의 Numpy 라이브러리는 List와 상호 변환이 가능하다.

```
import numpy as np

array = np.array([1,2,3])
print(array.size)
print(array.dtype)
print(array[2])

# 3
# int64
# 3
```

### 다양한 형태의 배열을 초기화 할 수 있다.

```
import numpy as np

# 0부터 3까지의 배열 만들기
array1 = np.arange(4)
print(array1)
# [0 1 2 3]

# 0으로 초기화
array2 = np.zeros((4,4),dtype=float)
print(array2)
# [[0. 0. 0. 0.]
# [0. 0. 0. 0.]
# [0. 0. 0. 0.]
# [0. 0. 0. 0.]]

# 1로 초기화
array3 = np.ones((3,3),dtype=str)
print(array3)
# [['1' '1' '1']
#  ['1' '1' '1']
#  ['1' '1' '1']]

# 0부터 9까지 랜덤하게 초기화 된 배열 만들기
array4 = np.random.randint(0,10,(3,3))
print(array4)
# [[1 6 9]
#  [6 2 3]
#  [4 6 8]]

# 평균이 0이고 표준편차가 1인 표준 정규를 띄는 배열
array5 = np.random.normal(0,1,(3,3))
print(array5)
# [[ 1.6310677  -1.34905038 -0.32447827]
#  [ 0.64019863  0.11859613  1.17303495]
#  [ 0.58201735  0.99960832  1.46972616]]
````

### 다양한 형태로 합치기

```
array1 = np.array([1,2,3])
array2 = np.array([4,5,6])
array3 = np.concatenate([array1, array2])

print(array3.shape)
print(array3)
# (6,)  6개의 데이터가 담겨있다.
# [1 2 3 4 5 6]
```

```
array1 = np.arange(4).reshape(1,4)
array2 = np.arange(8).reshape(2,4)
array3 = np.concatenate([array1,array2], axis=0)

print(array3.shape)
print(array3)
# (3, 4)
#[[0 1 2 3]
# [0 1 2 3]
# [4 5 6 7]]
```

### Numpy의 형태를 변경
```
array1 = np.arange(1,5).reshape(1,4)
print(array1)
array2 = array1.reshape(2,2)
print(array2.shape)
# [[1 2 3 4]]
# (2, 2)
```

```
array = np.arange(8).reshape(2,4)
left,right = np.split(array, [2], axis=1)

print(left.shape)
print(right.shape)
print(right[1][1])
# (2, 2)
# (2, 2)
# 7
```
###### axis의 기본 개념
* axis=0: 행(row) 방향
* axis=1: 열(column) 방향 으로 절단선을 긋는다고 생각하면 된다.


















