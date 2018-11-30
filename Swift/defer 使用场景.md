# defer 使用场景

- 任何scope里面都可以使用
- 释放资源
- 无论哪个分支最后都会被调用，给外界一个明确回复
- 多个defer类似于栈，后入先出
- 必须先自行了defer，最后才会被调用。即注册defer语句之前，就return了就不会被调用


[网址](https://www.jianshu.com/p/7c7f4b4e4efe)