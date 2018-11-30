# 实现一个 min 函数，返回两个元素较小的元素

主要考验泛型的使用
```
func getMin<T: Comparable>(a: T, b: T) -> T {
        return min(a, b)
    }
```
