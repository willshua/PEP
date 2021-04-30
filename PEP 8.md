## PEP 8: Python编码规范
原 文 地 址
: [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)

作 者
: Guido van Rossum (guido@python.org) <br> Barry Warsaw (barry@python.org) <br> Nick Coghlan (ncoghlan@gmail.com)

发 布 历 史
: 2001年7月5日 <br> 2013年8月1日


---

### 目录

- [导论](#1)
- [" A foolish consistency is the hobgoblin of little minds "](#2)
- [代码布局](#3)
- [字符串引号](#4)
- [表达式和语句中的空格](#5)
- [何时使用尾部逗号](#6)
- [注释](#7)
- [命名规范](#8)
- [编程建议](#9)
- [参考](#10)

---

#### 1. 导论 {#1}

---

#### 2. A foolish consistency is the hobgoblin of little minds {#2}

---

#### 3. 代码布局 {#3}

##### 3.1 缩进

* 每级缩进使用4个空格

```Python
# Correct:

# Aligned with open delimiter
foo = long_function_name(var_one, var_two,
                         var_three, var_four)

# Add 4 spaces (an extra level of indentation) to distinguish arguments from the rest.
def long_function_name(
        var_one, var_two, var_three, 
        var_four):
    print(var_one)

# Hanging indents should add a level.
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)
```

```Python
# Wrong:

# Arguments on first line forbidden when not using vertical alignment.
foo = long_function_name(var_one, var_two,
    var_three, var_four)

# Further identation required as indentation is not distinguishable.
def long_function_name(
    var_one, var_two, var_three,
    var_four):
    print(var_one)
```

* 对于连续行来说, 4个空格是规则是可选的.

```Python
# Hanging indents *may* be indented to other than 4 spaces.
foo = long_function_name(
  var_one, var_two,
  var_three, var_four)
```

```Python
# No extra indentation.
if (this_is_one_thing and
    that_is_another_thing):
    do_something()

# Add a comment, which will provide some distinction in editors supporting syntax highlighting.
if (this_is_one_thing and
    that_is_another_thing):
    # Since both conditions are true, we can frobnicate.
    do_something()

# Add some extra indentation on the conditional continuation line.
if (this_is_one_thing
        and that_is_another_thing):
    do_something()
```

```Python
my_list = [
    1, 2, 3,
    4, 5, 6,
    ]
result = some_function_that_takes_arguments(
    "a", "b", "c",
    "d", "e", "f",
    )
```


```Python
my_list = [
    1, 2, 3,
    4, 5, 6,
]
result = some_function_that_takes_arguments(
    "a", "b", "c",
    "d", "e", "f",
)
```


##### 3.2 Tabs还是空格

##### 3.3 行的最大长度

##### 3.4 应该在二元操作符前还是其后换行

##### 3.5 空行

##### 3.6 源文件编码

##### 3.7 库的导入

##### 3.8 模块级别的内置属性

---

#### 4. 字符串引号 {#4}

---

#### 5. 表达式和语句中的空格 {#5}

---

#### 6. 何时使用尾部逗号 {#6}

---

#### 7. 注释 {#7}

---

#### 8. 命名规范 {#8}

---

#### 9. 编程建议 {#9}

---

#### 10. 参考 {#10}

> [1] [PEP 7](https://www.python.org/dev/peps/pep-0007), Style Guide for C Code, van Rossum
> [2] Barry's GNU Mailman Style Guide <http://barry.warsaw.us/software/STYLEGUIDE.txt>
> [3] Donald Knuth's The TeXBook, pages 195 and 196.
> [4] <http://www.wikipedia.com/wiki/CamelCase>
> [5] Typeshed Repo <https://github.com/python/typeshed>
> [6] Suggested Syntax for Python 2.7 and Straddling Code <https://www.python.org/dev/peps/pep-0484/#suggested-syntax-for-python-2-7-and-straddling-code>
