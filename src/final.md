# final

    final：修饰符（关键字）有三种用法：
    1. 如果一个类被声明为final，意味着它不能再派生出新的子类，即不能被继承，因此它和 abstract 是反义词。
    2. 将变量声明为 final，可以保证它们在使用中不被改变，被声明为 final 的变量必须在声明时给定初值，而在以后的引用中只能读取不可修改。
    3. 被声明为 final 的方法也同样只能使用，不能在子类中被重写。


## 空白final 
Java允许生成“空白final”，所谓空白final是指被声明为final但又未给定初值的域。无论什么情况，编译器都确保空白final在**使用前必须被初始化**。但是，空白final在关键字final的使用上提供了更大的灵活性，为此，一个类中的final域就可以做到根据对象而有所不同，却又保持其恒定不变的特性。
