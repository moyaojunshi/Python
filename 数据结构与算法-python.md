



数据结构与算法--Python

## 1.基本概念

### 1.0算法的五大特性

> **输入**: 算法具有0个或多个输入
>
> **输出**: 算法至少有1个或多个输出
>
> **有穷性**: 算法在有限的步骤之后会自动结束而不会无限循环，并且每一个步骤可以在可接受的时间内完
>
> **确定性**：算法中的每一步都有确定的含义，不会出现二义性
>
> **可行性**：算法的每一步都是可行的，也就是说每一步都能够执行有限的次数完成

### 1.1时间复杂度

### 1.2空间复杂度

### 1.3基本流程

> 1.3.0理解题目
>
> 1.3.1确定测试用例
>
> 1.3.2确定思路
>
> 1.3.3确定数据结构
>
> 1.3.4定义参数（常量/变量）
>
> > 赋值方法：
> >
> > * 常量只有一个取值，直接赋值，
> >
> >   * ```
> >     a = 1
> >     ```
> >
> >     ---
> >
> >     
> >
> > * 常量可能有多个取值，迭代赋值
> >
> >   * ```
> >     for a in range(0, 1001):
> >     print(a)
> >     ```
> >
> >     ---
> >
> >     
> >   * ```
> >  list = [1, 2, 5, 9, 0]
> >  it = iter(list)
> >   
> >   # print(next(it)) # 按顺序单点打印
> >  
> >    for a in range(0, len(list)):
> >        print(next(it))
> >  ```
> >
> > 
>
> 1.3.5构建实现方法
>
> 1.3.6多场景测试并优化方法

### 1.4.常见的数据结构

> 1.链表
>
> 2.栈
>
> 3.队列
>
> 4.二叉树

### 1.5.常见的数据类型及其增删改查

> Python中常见的数据类型有数字、字符串、列表、元组、字典、集合
>
> 常见的数据运算操作是：增/插入、删、改、查、排序

#### 1.5.1数字

> 删
>
> > del var
>
> 类型转换
>
> > int(x)
> >
> > float(x)
> >
> > complex(x)
>
> 数学函数
>
> >| 函数                              | 返回值                                                       |
> >| --------------------------------- | ------------------------------------------------------------ |
> >| abs(x)                            | 绝对值\|x\|                                                  |
> >| log(x)                            | 如math.log(math.e)返回1.0,math.log(100,10)返回2.0            |
> >| log10(x)                          | 返回以10为基数的x的对数，如math.log10(100)返回 2.0           |
> >| $max(x_{1},x_{2},,,,x_{n})$       | 返回给定参数的最大值，参数可以为序列。                       |
> >| $min(x_{1},x_{2},,,,x_{n})$       | 返回给定参数的最小值，参数可以为序列。                       |
> >| pow(x,y)                          | 返回$x^{y}$                                                  |
> >| sqrt(x)                           | $\sqrt{x}$                                                   |
> >| choice(seq)                       | 从序列的元素中随机挑选一个元素，比如random.choice(range(10))，从0到9中随机挑选一个整数。 |
> >| randrange([start, ] stop [,step]) | 从指定范围内，按指定基数递增的集合中获取一个随机数，基数默认值为 1 |
> >| random()                          | 随机生成下一个实数，它在[0,1)范围内                          |
> >| seed([x])                         | 改变随机数生成器的种子seed。如果你不了解其原理，你不必特别去设定seed，Python会帮你选择seed。 |
> >| shuffle(lst)                      | 将序列的所有元素随机排序                                     |
> >| uniform(x,y)                      | 随机生成下一个实数，它在[x,y]范围内。                        |

#### 1.5.2字符串

>增
>
>> **用+拼接**
>>
>> ```
>> a, b = "hello", "wold"
>> print(a + b)
>> # hellowold
>> ```
>>
>> 
>
>删
>
>str.strip()分割
>
>描述：方法把字符串以某个字符划分为若干个部分
>
>输出结果：list
>
>> ```
>> str = 'www.google.com'
>> str_split = str.split('.')
>> print(str_split)
>> 
>> # ['www', 'google', 'com']
>> # 返回值是列表
>> ```
>
>改
>
>>replace()替换
>>
>>描  述：方法把字符串的原字符串替换成新字符串。
>>
>>输出结果：str
>>
>>```
>>str = "www.google.com"
>>print(str.replace("."," "))
>>
>># www google com
>>```
>
>查
>
>>1.索引
>>
>>2.切片
>>
>>3.find() 查找
>>
>>* 描  述：检测字符串中是否包含想要查找的**字符**。如果包含字符返回该字符串首个字符索引值，否则返回-1
>>
>>* 输出结果：索引或-1
>>
>>	>```
>>	>str = "www.google.com"
>>	>print(str.find("com"))
>>	>
>>	># 11
>>	>```
>
>常用函数
>
>>| 函数                    | 描述                                                         | 例子                                                         |
>>| ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
>>| count()                 | 输出结果：Int                                                | name = 'chenxin'<br/>name1 = name.count('e',0,4)<br/>print(name1)<br/>结    果：<br/>1 |
>>| lower() <br/>S.upper()  | 描  述：lower()转换字符串所有大写字符为小写<br/>输出结果：字符串str | name = "CHENXIN"<br/>name1 = name.lower()<br/>print(name1)<br/>结果：<br/>chenxin<br/> <br/>S.upper()将所有小写转换为大写<br/>返回S字符串的大写格式。<br/>str = "Www.Google.com"<br/>print(str.upper())<br/>结果：<br/>WWW.GOOGLE.COM |
>>| capitalize()            | 描  述：将字符串的第一个字母变为大写字母（不是每个单词的首字母，而是一对双引号引起来的一组字符串）<br/>输出结果；str | str = "www.google.com"<br/>print(str.capitalize())<br/>结果：<br/>Www.google.com |
>>| title()                 | 描  述：方法标题化的字符串，就是说所有单词都是以大写开始，其余字母均为小写。<br/>输出结果：str | str = "www google com"<br/>print(str.title())<br/>结果：<br/>Www Google Com |
>>| startswith()            | 描  述：方法用于判断字符串是否是以指定的字符串开头<br/>输出结果：Ture，False | str = "www google com"<br/>print(str.startswith("w"))<br/>结果：<br/>True |
>>| endswith()              | 描  述：方法用于判断字符串是否以指定后缀结尾。<br/>输出结果：Ture，False | str = "www.google.com"<br/>print(str.endswith("m"))<br/>结果：<br/>True |
>>| islower() <br/>isuppe() | islower()判断是否由小写字母组成<br/>isuppe()判断是否都是大写<br/>输出结果：True，False | str = "www.google.com"<br/>print(str.islower())<br/>结果：<br/>True |
>>



#### 1.5.3列表

> | 列表的操作 | 方法         | 描述                                                         |
> | ---------- | ------------ | ------------------------------------------------------------ |
> | 增         | append       | 追加，在列表的尾部加入指定的元素                             |
> | 增         | extend       | 将指定序列的元素依次追加到列表的尾部(合并),不会去重复内容    |
> |            | insert       | 将对象插入列表                                               |
> | 删         | pop          | 弹出，返回并删除指定索引位上的数据，默认删除索引为-1的数据(从右向左删除) |
> | 删         | remove       | 从左往右删除一个指定的元素                                   |
> | 删         | del          | 删除整个列表或列表的数据，del是python内置功能，不是列表独有的 |
> | 查         | list.index   | 查找，从左往右返回查找到的第一个指定元素的索引，如果没有找到，报错 |
> | 查         | 索引/切片    |                                                              |
> | 排         | list.reverse | 顺序倒序                                                     |
> | 排         | list.sort    | 按照ascii码表顺序进行排序                                    |
>
> 函数
>
> | 函数      | 描述                                             |
> | --------- | ------------------------------------------------ |
> | len(list) | 描述：返回列表元素个数<br/>返回结果：int         |
> | max(list) | 描述：获取列表中最大的数字<br/>返回结果：number  |
> | min(list) | 描述：获取列表中最小的数字<br/>返回结果：number  |
> | list(set) | 描述：将列表转换为元组并去重<br/>返回结果：tuple |

#### 1.5.4元组

> | 元组操作 | 方法           | 描述   |
> | -------- | -------------- | ------ |
> | 查       | 索引/切片/遍历 |        |
> | 查       | index()        | 求索引 |
>
>  元组特点：元组是有序的，不能修改 

#### 1.5.5字典

>  字典特征：无序、键名是唯一的，元素采用键值对的形式进行存储，字典属于可变数据类型。 
>
> | 字典操作 | 方法                                                  | 描述                                                         |
> | -------- | ----------------------------------------------------- | ------------------------------------------------------------ |
> | 增       | dict[key] = value                                     |                                                              |
> | 删       | del dict(key) <br/>dict.pop(key)<br/>popitem ( )<br/> | 随机删除一对键和值：popitem ( ) 字典popitem()方法作用是：随机返回并删除字典中的一对键和值（项）。为什么是随机删除呢？因为字典是无序的，没有所谓的“最后一项”或是其它顺序。在工作时如果遇到需要逐一删除项的工作，用popitem()方法效率很高 |
> | 改       | dict[key] = value                                     | 有则修改，无则添加                                           |
> | 查       | 直接根据键名查询                                      |                                                              |
> | 查       | dic.keys                                              | 查询所有的键名                                               |
> | 查       | dic.values                                            | 查询所有的键的值                                             |





## 2.链表

### 2.1单向链表

>  单向链表也叫单链表，是链表中最简单的一种形式，它的每个节点包含两个域，一个信息域（元素域）和一个链接域。这个链接指向链表中的下一个节点，而最后一个节点的链接域则指向一个空值 
>
> - 表元素域elem用来存放具体的数据。
> - 链接域next用来存放下一个节点的位置（python中的标识）
> - 变量p指向链表的头节点（首节点）的位置，从p出发能找到表中的任意节点。

### 2.2节点实现

```python
class SingleNode(object):
    """单链表的结点"""
    def __init__(self,item):
        # item存放数据元素
        self.item = item
        # next是下一个节点的标识
        self.next = None
```

### 2.3单链表的操作

> - is_empty() 链表是否为空
> - length() 链表长度
> - travel() 遍历整个链表
> - add(item) 链表头部添加元素
> - append(item) 链表尾部添加元素
> - insert(pos, item) 指定位置添加元素
> - remove(item) 删除节点
> - search(item) 查找节点是否存在

### 2.4单链表的实现

> ```python
> class SingleLinkList(object):
>     """单链表"""
>     def __init__(self):
>         self.__head = None
> 
>     def is_empty(self):
>         """判断链表是否为空"""
>         return self.__head == None
> 
>     def length(self):
>         """链表长度"""
>         # cur初始时指向头节点
>         cur = self.__head
>         count = 0
>         # 尾节点指向None，当未到达尾部时
>         while cur != None:
>             count += 1
>             # 将cur后移一个节点
>             cur = cur.next
>         return count
> 
>     def travel(self):
>         """遍历链表"""
>         cur = self.__head
>         while cur != None:
>             print(cur.item,)
>             cur = cur.next
> ```
>
> **头部添加元素**
>
> ```python
>     def add(self, item):
>         """头部添加元素"""
>         # 先创建一个保存item值的节点
>         node = SingleNode(item)
>         # 将新节点的链接域next指向头节点，即_head指向的位置
>         node.next = self.__head
>         # 将链表的头_head指向新节点
>         self.__head = node
> ```
>
> **尾部添加元素**
>
> ```python
>     def append(self, item):
>         """尾部添加元素"""
>         node = SingleNode(item)
>         # 先判断链表是否为空，若是空链表，则将_head指向新节点
>         if self.is_empty():
>             self.__head = node
>         # 若不为空，则找到尾部，将尾节点的next指向新节点
>         else:
>             cur = self.__head
>             while cur.next != None:
>                 cur = cur.next
>             cur.next = node
> ```
>
> **指定位置添加元素**
>
> ```python
>     def insert(self, pos, item):
>         """指定位置添加元素"""
>         # 若指定位置pos为第一个元素之前，则执行头部插入
>         if pos <= 0:
>             self.add(item)
>         # 若指定位置超过链表尾部，则执行尾部插入
>         elif pos > (self.length()-1):
>             self.append(item)
>         # 找到指定位置
>         else:
>             node = SingleNode(item)
>             count = 0
>             # pre用来指向指定位置pos的前一个位置pos-1，初始从头节点开始移动到指定位置
>             pre = self.__head
>             while count < (pos-1):
>                 count += 1
>                 pre = pre.next
>             # 先将新节点node的next指向插入位置的节点
>             node.next = pre.next
>             # 将插入位置的前一个节点的next指向新节点
>             pre.next = node
> ```
>
> **删除节点**
>
> ```python
> def remove(self,item):
>         """删除节点"""
>         cur = self.__head
>         pre = None
>         while cur != None:
>             # 找到了指定元素
>             if cur.item == item:
>                 # 如果第一个就是删除的节点
>                 if not pre:
>                     # 将头指针指向头节点的后一个节点
>                     self.__head = cur.next
>                 else:
>                     # 将删除位置前一个节点的next指向删除位置的后一个节点
>                     pre.next = cur.next
>                 break
>             else:
>                 # 继续按链表后移节点
>                 pre = cur
>                 cur = cur.next
> ```
>
> **查找节点是否存在** 
>
> ```python
>     def search(self,item):
>         """链表查找节点是否存在，并返回True或者False"""
>         cur = self.__head
>         while cur != None:
>             if cur.item == item:
>                 return True
>             cur = cur.next
>         return False
> ```
>
> **测试**
>
> ```python
> if __name__ == "__main__":
>     ll = SingleLinkList()
>     ll.add(1)
>     ll.add(2)
>     ll.append(3)
>     ll.insert(2, 4)
>     print "length:",ll.length()
>     ll.travel()
>     print ll.search(3)
>     print ll.search(5)
>     ll.remove(1)
>     print "length:",ll.length()
>     ll.travel()
> ```



## 3.栈

### 栈的操作

- Stack() 创建一个新的空栈
- push(item) 添加一个新的元素item到栈顶
- pop() 弹出栈顶元素
- peek() 返回栈顶元素
- is_empty() 判断栈是否为空
- size() 返回栈的元素个数

```python
class Stack(object):
    """栈"""
    def __init__(self):
         self.items = []

    def is_empty(self):
        """判断是否为空"""
        return self.items == []

    def push(self, item):
        """加入元素"""
        self.items.append(item)

    def pop(self):
        """弹出元素"""
        return self.items.pop()

    def peek(self):
        """返回栈顶元素"""
        return self.items[len(self.items)-1]

    def size(self):
        """返回栈的大小"""
        return len(self.items)

if __name__ == "__main__":
    stack = Stack()
    stack.push("hello")
    stack.push("world")
    stack.push("itcast")
    print stack.size()
    print stack.peek()
    print stack.pop()
    print stack.pop()
    print stack.pop()
```



## 4.队列

### 操作

- Queue() 创建一个空的队列
- enqueue(item) 往队列中添加一个item元素
- dequeue() 从队列头部删除一个元素
- is_empty() 判断一个队列是否为空
- size() 返回队列的大小

```python
class Queue(object):
    """队列"""
    def __init__(self):
        self.items = []

    def is_empty(self):
        return self.items == []

    def enqueue(self, item):
        """进队列"""
        self.items.insert(0,item)

    def dequeue(self):
        """出队列"""
        return self.items.pop()

    def size(self):
        """返回大小"""
        return len(self.items)

if __name__ == "__main__":
    q = Queue()
    q.enqueue("hello")
    q.enqueue("world")
    q.enqueue("itcast")
    print q.size()
    print q.dequeue()
    print q.dequeue()
    print q.dequeue()
```



## 5.二叉树

### 5.1二叉树的节点表示以及树的创建

>  通过使用Node类中定义三个属性，分别为elem本身的值，还有lchild左孩子和rchild右孩子 
>
> ```python
> class Node(object):
>     """节点类"""
>     def __init__(self, elem=-1, lchild=None, rchild=None):
>         self.elem = elem
>         self.lchild = lchild
>         self.rchild = rchild
> ```
>
>  树的创建,创建一个树的类，并给一个root根节点，一开始为空，随后添加节点 
>
> ```python
> class Tree(object):
>     """树类"""
>     def __init__(self, root=None):
>         self.root = root
> 
>     def add(self, elem):
>         """为树添加节点"""
>         node = Node(elem)
>         #如果树是空的，则对根节点赋值
>         if self.root == None:
>             self.root = node
>         else:
>             queue = []
>             queue.append(self.root)
>             #对已有的节点进行层次遍历
>             while queue:
>                 #弹出队列的第一个元素
>                 cur = queue.pop(0)
>                 if cur.lchild == None:
>                     cur.lchild = node
>                     return
>                 elif cur.rchild == None:
>                     cur.rchild = node
>                     return
>                 else:
>                     #如果左右子树都不为空，加入队列继续判断
>                     queue.append(cur.lchild)
>                     queue.append(cur.rchild)
> ```

### 5.2二叉树的遍历

> #### 深度优先遍历
>
> 对于一颗二叉树，深度优先搜索(Depth First Search)是沿着树的深度遍历树的节点，尽可能深的搜索树的分支。
> 那么深度遍历有重要的三种方法。这三种方式常被用于访问树的节点，它们之间的不同在于访问每个节点的次序不同。这三种遍历分别叫做先序遍历（preorder），中序遍历（inorder）和后序遍历（postorder）。我们来给出它们的详细定义，然后举例看看它们的应用。
>
> - 先序遍历 在先序遍历中，我们先访问根节点，然后递归使用先序遍历访问左子树，再递归使用先序遍历访问右子树
> 根节点->左子树->右子树
>
> - ```python
> def preorder(self, root):
>      """递归实现先序遍历"""
>      if root == None:
>          return
>      print root.elem
>      self.preorder(root.lchild)
>      self.preorder(root.rchild)
>   ```
> ```
> 
> -  中序遍历 在中序遍历中，我们递归使用中序遍历访问左子树，然后访问根节点，最后再递归使用中序遍历访问右子树
> 左子树->根节点->右子树 
> 
> - ```python
> def inorder(self, root):
>      """递归实现中序遍历"""
>      if root == None:
>          return
>      self.inorder(root.lchild)
>      print root.elem
>      self.inorder(root.rchild)
> ```
>
> -  后序遍历 在后序遍历中，我们先递归使用后序遍历访问左子树和右子树，最后访问根节点
> 左子树->右子树->根节点 
>
> - ```python
> def postorder(self, root):
>      """递归实现后续遍历"""
>      if root == None:
>          return
>      self.postorder(root.lchild)
>      self.postorder(root.rchild)
>      print root.elem
>   ```
> ```
> 
> #### 广度优先遍历(层次遍历)
> 
> 从树的root开始，从上到下从从左到右遍历整个树的节点
> 
> ​```python
> def breadth_travel(self):
>      """利用队列实现树的层次遍历"""
>      if root == None:
>          return
>      queue = []
>      queue.append(root)
>      while queue:
>          node = queue.pop(0)
>          print node.elem,
>          if node.lchild != None:
>              queue.append(node.lchild)
>          if node.rchild != None:
>              queue.append(node.rchild)
> ```
>
> 

## 6.排序

### 6.1冒泡排序

> **冒泡排序**（英语：Bubble Sort）是一种简单的排序算法。它重复地遍历要排序的数列，一次比较两个元素，如果他们的顺序错误就把他们交换过来。遍历数列的工作是重复地进行直到没有再需要交换，也就是说该数列已经排序完成。这个算法的名字由来是因为越小的元素会经由交换慢慢“浮”到数列的顶端。
>
> 冒泡排序算法的运作如下：
>
> - 比较相邻的元素。如果第一个比第二个大（升序），就交换他们两个。
> - 对每一对相邻元素作同样的工作，从开始第一对到结尾的最后一对。这步做完后，最后的元素会是最大的数。
> - 针对所有的元素重复以上的步骤，除了最后一个。
> - 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。
>
> ```python
> def bubble_sort(alist):
>     for j in range(len(alist)-1,0,-1):
>         # j表示每次遍历需要比较的次数，是逐渐减小的
>         for i in range(j):
>             if alist[i] > alist[i+1]:
>                 alist[i], alist[i+1] = alist[i+1], alist[i]
> 
> li = [54,26,93,17,77,31,44,55,20]
> bubble_sort(li)
> print(li)
> ```
>
> **时间复杂度**
>
> - 最优时间复杂度：O(n) （表示遍历一次发现没有任何可以交换的元素，排序结束。）
> - 最坏时间复杂度：O(n2)
> - 稳定性：稳定

### 6.2选择排序

> 选择排序（Selection sort）是一种简单直观的排序算法。它的工作原理如下。首先在未排序序列中找到最小（大）元素，存放到排序序列的起始位置，然后，再从剩余未排序元素中继续寻找最小（大）元素，然后放到已排序序列的末尾。以此类推，直到所有元素均排序完毕。
>
> 选择排序的主要优点与数据移动有关。如果某个元素位于正确的最终位置上，则它不会被移动。选择排序每次交换一对元素，它们当中至少有一个将被移到其最终位置上，因此对n个元素的表进行排序总共进行至多n-1次交换。在所有的完全依靠交换去移动元素的排序方法中，选择排序属于非常好的一种
>
> ```python
> def selection_sort(alist):
>     n = len(alist)
>     # 需要进行n-1次选择操作
>     for i in range(n-1):
>         # 记录最小位置
>         min_index = i
>         # 从i+1位置到末尾选择出最小数据
>         for j in range(i+1, n):
>             if alist[j] < alist[min_index]:
>                 min_index = j
>         # 如果选择出的数据不在正确位置，进行交换
>         if min_index != i:
>             alist[i], alist[min_index] = alist[min_index], alist[i]
> 
> alist = [54,226,93,17,77,31,44,55,20]
> selection_sort(alist)
> print(alist)
> ```
>
> **时间复杂度**
>
> - 最优时间复杂度：$O(n^{2})$
> - 最坏时间复杂度：$O(n^{2})$
> - 稳定性：不稳定（考虑升序每次选择最大的情况）

### 6.3插入排序

> 插入排序（英语：Insertion Sort）是一种简单直观的排序算法。它的工作原理是通过构建有序序列，对于未排序数据，在已排序序列中从后向前扫描，找到相应位置并插入。插入排序在实现上，在从后向前扫描过程中，需要反复把已排序元素逐步向后挪位，为最新元素提供插入空间。
>
> ```python
> def insert_sort(alist):
>     # 从第二个位置，即下标为1的元素开始向前插入
>     for i in range(1, len(alist)):
>         # 从第i个元素开始向前比较，如果小于前一个元素，交换位置
>         for j in range(i, 0, -1):
>             if alist[j] < alist[j-1]:
>                 alist[j], alist[j-1] = alist[j-1], alist[j]
> 
> alist = [54,26,93,17,77,31,44,55,20]
> insert_sort(alist)
> print(alist)
> ```
>
> **时间复杂度**
>
> - 最优时间复杂度：O(n) （升序排列，序列已经处于升序状态）
> - 最坏时间复杂度：O(n2)
> - 稳定性：稳定

### 6.4快速排序

> 快速排序（英语：Quicksort），又称划分交换排序（partition-exchange sort），通过一趟排序将要排序的数据分割成独立的两部分，其中一部分的所有数据都比另外一部分的所有数据都要小，然后再按此方法对这两部分数据分别进行快速排序，整个排序过程可以递归进行，以此达到整个数据变成有序序列。
>
> > 步骤为：
>
> 1. 从数列中挑出一个元素，称为"基准"（pivot），
> 2. 重新排序数列，所有元素比基准值小的摆放在基准前面，所有元素比基准值大的摆在基准的后面（相同的数可以到任一边）。在这个分区结束之后，该基准就处于数列的中间位置。这个称为分区（partition）操作。
> 3. 递归地（recursive）把小于基准值元素的子数列和大于基准值元素的子数列排序。
>
> 递归的最底部情形，是数列的大小是零或一，也就是永远都已经被排序好了。虽然一直递归下去，但是这个算法总会结束，因为在每次的迭代（iteration）中，它至少会把一个元素摆到它最后的位置去。
>
> ```python
> def quick_sort(alist, start, end):
>     """快速排序"""
> 
>     # 递归的退出条件
>     if start >= end:
>         return
> 
>     # 设定起始元素为要寻找位置的基准元素
>     mid = alist[start]
> 
>     # low为序列左边的由左向右移动的游标
>     low = start
> 
>     # high为序列右边的由右向左移动的游标
>     high = end
> 
>     while low < high:
>         # 如果low与high未重合，high指向的元素不比基准元素小，则high向左移动
>         while low < high and alist[high] >= mid:
>             high -= 1
>         # 将high指向的元素放到low的位置上
>         alist[low] = alist[high]
> 
>         # 如果low与high未重合，low指向的元素比基准元素小，则low向右移动
>         while low < high and alist[low] < mid:
>             low += 1
>         # 将low指向的元素放到high的位置上
>         alist[high] = alist[low]
> 
>     # 退出循环后，low与high重合，此时所指位置为基准元素的正确位置
>     # 将基准元素放到该位置
>     alist[low] = mid
> 
>     # 对基准元素左边的子序列进行快速排序
>     quick_sort(alist, start, low-1)
> 
>     # 对基准元素右边的子序列进行快速排序
>     quick_sort(alist, low+1, end)
> 
> 
> alist = [54,26,93,17,77,31,44,55,20]
> quick_sort(alist,0,len(alist)-1)
> print(alist)
> ```
>
> **时间复杂度**
>
> - 最优时间复杂度：O(nlogn)
> - 最坏时间复杂度：O(n2)
> - 稳定性：不稳定

## 7.搜索

>  搜索是在一个项目集合中找到一个特定项目的算法过程。搜索通常的答案是真的或假的，因为该项目是否存在。 搜索的几种常见方法：顺序查找、二分法查找、二叉树查找、哈希查找 

### 7.1 二分查找

> ## 二分法查找
>
> 二分查找又称折半查找，优点是比较次数少，查找速度快，平均性能好；其缺点是要求待查表为有序表，且插入删除困难。因此，折半查找方法适用于不经常变动而查找频繁的有序列表。首先，假设表中元素是按升序排列，将表中间位置记录的关键字与查找关键字比较，如果两者相等，则查找成功；否则利用中间位置记录将表分成前、后两个子表，如果中间位置记录的关键字大于查找关键字，则进一步查找前一子表，否则进一步查找后一子表。重复以上过程，直到找到满足条件的记录，使查找成功，或直到子表不存在为止，此时查找不成功。
>
> **非递归实现**
>
> ```python
> def binary_search(alist, item):
>       first = 0
>       last = len(alist)-1
>       while first<=last:
>           midpoint = (first + last)/2
>           if alist[midpoint] == item:
>               return True
>           elif item < alist[midpoint]:
>               last = midpoint-1
>           else:
>               first = midpoint+1
>     return False
> testlist = [0, 1, 2, 8, 13, 17, 19, 32, 42,]
> print(binary_search(testlist, 3))
> print(binary_search(testlist, 13))
> ```
>
> **递归实现**
>
> ```python
> def binary_search(alist, item):
>     if len(alist) == 0:
>         return False
>     else:
>         midpoint = len(alist)//2
>         if alist[midpoint]==item:
>           return True
>         else:
>           if item<alist[midpoint]:
>             return binary_search(alist[:midpoint],item)
>           else:
>             return binary_search(alist[midpoint+1:],item)
> 
> testlist = [0, 1, 2, 8, 13, 17, 19, 32, 42,]
> print(binary_search(testlist, 3))
> print(binary_search(testlist, 13))
> ```
>
> **时间复杂度**
>
> - 最优时间复杂度：O(1)
> - 最坏时间复杂度：O(logn)



