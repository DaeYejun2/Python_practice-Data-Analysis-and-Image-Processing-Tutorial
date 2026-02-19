# Numpy의 활용

### 저장 및 불러오기가 가능하다

```
array = np.arange(0,10)
np.save('save.npy',array)

result = np.load('save.npy')
print(result)
# [0 1 2 3 4 5 6 7 8 9]
```
#### 여러개도 가능
```
array1 = np.arange(0, 10)
array2 = np.arange(10, 20)
np.savez('saved.npz', array1=array1, array2=array2)

data = np.load('saved.npz')
result1 = data['array1']
result2 = data['array2']
print(result1)
print(result2)
# [0 1 2 3 4 5 6 7 8 9]
# [10 11 12 13 14 15 16 17 18 19]
```

### 정렬
```

# Numpy 원소 오름차순 정렬
array = np.array([5, 9, 10, 3, 1])
array.sort()
print(array)

# Numpy 원소 내림차순 정렬
array = np.array([5, 9, 10, 3, 1])
array.sort()
print(array[::-1])

# 열을 기준으로 정렬
array = np.array([[5, 9, 10, 3, 1], [8, 3, 4, 2, 5]])
array.sort(axis=0)
print(array)
# [[ 5  3  4  2  1]
#  [ 8  9 10  3  5]]
```

### 자주 사용하는 함수
```
# 균일한 간격으로 데이터 생성
array = np.linspace(0,10,5)
print(array)
# [ 0.   2.5  5.   7.5 10. ]

# 난수의 재연
np.random.seed(7)
print(np.random.randint(0,10,(2,3)))
# [[4 9 6]
#  [3 3 7]]

# Numpy 배열 객체 복사
array1 = np.arange(0,10)
array2 = array1.copy()
print(array2)
# [0 1 2 3 4 5 6 7 8 9]

# 중복된 원소 제거
array = np.array([1,1,2,3,3,3,1])
print(np.unique(array))
# [1 2 3]
```





