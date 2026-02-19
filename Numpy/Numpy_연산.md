# Numpy의 연산과 함수

### 기본적인 상수 연산
```
array = np.random.randint(1, 10, size=4).reshape(2,2)
result_array = array*10
print(result_array)
# [[20 40]
# [40 30]]
```

### 서로 다른 형태의 Numpy 연산
```
array1 = np.arange(4).reshape(2,2)
# [[0 1]
#  [2 3]]
array2 = np.arange(2)
# [0 1]
array3 = array1+array2

print(array3)
# [[0 2]
#  [2 4]]
```
```
array1 = np.arange(0,8).reshape(2,4)
array2 = np.arange(0,8).reshape(2,4)
array3 = np.concatenate([array1,array2],axis=0)
print(array3)
# [[0 1 2 3]
#  [4 5 6 7]
#  [0 1 2 3]
#  [4 5 6 7]]
array4 = np.arange(0,4).reshape(4,1)
print(array4)
# [[0]
#  [1]
#  [2]
#  [3]]

print(array3+array4)
# [[ 0  1  2  3]
#  [ 5  6  7  8]
#  [ 2  3  4  5]
#  [ 7  8  9 10]]
```

### 마스킹 연산이 가능하다

#### Numpy 원소의 값을 조건에 따라 바꿀 때 사용
#### 대체로 이미지 처리에서 자주 활용

```
array1 = np.arange(16).reshape(4,4)
print(array1)
# [[ 0  1  2  3]
#  [ 4  5  6  7]
#  [ 8  9 10 11]
#  [12 13 14 15]]

array2 = array1 < 10
print(array2)
# [[ True  True  True  True]
#  [ True  True  True  True]
#  [ True  True False False]
#  [False False False False]]

array1[array2] = 100
print(array1)
# [[100 100 100 100]
#  [100 100 100 100]
#  [100 100  10  11]
#  [ 12  13  14  15]]
```

### 집계 함수
```
array = np.arange(16).reshape(4,4)

print("최대값: ",np.max(array))
print("최소값: ",np.min(array))
print("합계: ",np.sum(array))
print("평균값: ",np.mean(array))
# 최대값:  15
# 최소값:  0
# 합계:  120
# 평균값:  7.5

print("합계: ",np.sum(array, axis=0))
합계: [24 28 32 36]
```


