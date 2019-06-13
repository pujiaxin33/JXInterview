# Optional（可选型） 是用什么实现的

我们使用的类型后加上 ? 的语法只不过是 Optional 类型的语法糖，而实际上这个类型是一个 enum：

enum Optional<T> : _Reflectable, NilLiteralConvertible {
    case None
    case Some(T)

    //...
}
在这个定义中，对 T 没有任何限制，也就是说，我们是可以在 Optional 中装入任意东西的，甚至也包括 Optional 对象自身。打个形象的比方，如果我们把 Optional 比作一个盒子，实际具体的 String 或者 Int 这样的值比作糖果的话，当我们打开一个盒子 (unwrap) 时，可能的结果会有三个 -- 空气，糖果，或者另一个盒子

[多重 OPTIONAL](https://swifter.tips/multiple-optional/)