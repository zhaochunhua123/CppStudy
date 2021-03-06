# auto 可能的适用场景

auto 是 c++11 提供的新的特性，它使用变量的初始值来自动推导变量的类型。因此定义的变量必须有初始值，才可以使用 auto 。

## 例子

```c++
auto i = 42;        // i 的类型是 int
double f();
auto d = f();       // d 的类型是 double
```

## 适用场景

上述的写法似乎不太理想，因为有时候明确的写出变量的类型更易于快速理解变量的功能。比如，变量是一个自定义类型的时候，如果使用的是 auto 推导，那么就要去思考它是什么。

如果类型很长，并且很容易知道它是什么，而没有必要知道它的完整写法的时候，就可以用 auto 。

比如：

```c++
// 使用 auto 得到迭代器类型
vector<string> v;
auto first = v.begin();

// 使用 auto 得到一个 lambda 对象的类型
auto l = [](int x)->bool { /* some code... */ };
```