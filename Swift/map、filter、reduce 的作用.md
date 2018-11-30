# map、filter、reduce 的作用

```
let numbers = [1, 3, 5, 4, 2]
//Returns an array containing the results of mapping the given closure over the sequence's elements.
//将数据中的对象进行映射，可以更换类型，多种维度解读数据，数量不会有变化。
let strings = numbers.map { (num) -> String in
    return String(num)
}
print(strings)//["1", "3", "5", "4", "2"]
//Returns an array containing, in order, the elements of the sequence that satisfy the given predicate.
//根据闭包里面的判定条件，过滤掉不符合的元素
let filterNumbers = numbers.filter { (num) -> Bool in
    return num > 3
}
print(filterNumbers)//[5, 4]
//Returns the result of combining the elements of the sequence using the given closure.
//整合序列中的元素，给出一个结果
let reduceResult = numbers.reduce(0) { (x, y) -> Int in
    return x + y
}
print(reduceResult)//15
```