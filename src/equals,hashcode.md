

# equals&&hashCode

源代码:

```java
@Override
public boolean equals(Object obj) {
    return super.equals(obj);
}

@Override
public int hashCode() {
    return super.hashCode();
}
```

如果父类重写equals和hashCode的话,子类也会重写。





### equals方法实现了等价关系（equivalence relation）：
- 自反性（reflexive）。对于任何非null引用值x，x.equals（x）必须返回true。
- 对称性（symmetric）。对于任何非null引用值x和y，当且仅当 y.equals（x）返回true时，X.equals（y）必须返回true。
- 传递性（transitive）。对于任何非null的引用值x、y和z，如果 x equals（y）返回true，并且 y. equals（z）也返回true，那么x.equals（z）也必须返回true。
- 一致性（consistent）。对于任何非null的引用值x和y，只要equals的比较操作在对象中所用的信息没有被修改，多次调用x.equals（y）就会一致地返回true，或者一致地返回false。对于任何非null的引用值x，x equals（null）必须返回false。



## equals与==的区别

== 是一个运算符。
Equals则是string对象的方法，可以.（点）出来。 

1.  基本数据类型比较 　
    ==比较两个值是否相等。相等为true 否则为false； equals不能直接用于基本类型的比较。需要将基本类型转换为包装器进行比较。
2. 引用对象比较 
   ==和equals都是比较栈内存中的地址是否相等 。相等为true 否则为false； 　 
   需注意几点：
3. string是一个特殊的引用类型。对于两个字符串的比较，不管是 == 和 equals 这两者比较的都是字符串是否相同；

4. 当你创建两个string对象时，内存中的地址是不相同的，你可以赋相同的值。 　　所以字符串的内容相同。引用地址不一定相同，（相同内容的对象地址不一定相同），但反过来却是肯定的；

5. 基本数据类型比较(string 除外) == 和 Equals 两者都是比较值；