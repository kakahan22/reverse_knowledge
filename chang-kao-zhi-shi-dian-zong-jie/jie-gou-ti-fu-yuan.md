---
description: 讲了三个星期就讲了这个der
---

# 🤨 结构体复原

## 1.基本结构体复原：

当我们在伪代码中看到很多的ptr+4,ptr+8,ptr+3,ptr+16这种的时候，我们就需要利用结构体复原了。

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

### ①创建结构体

windows->structures

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

然后按我们键盘上面的insert键就是插入一个新的结构体，delete就是删除结构体，然后给结构体命名，其他保持默认不变。

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

然后基本的结构体的框架就出来了。

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

### ②添加变量

然后我们往结构体里添加对象

#### Ⅰ少数

如果是少数的对象，我们只需要用快捷键d就可以完成。并且此时鼠标需要放在ends后面

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

我们可以看到此时添加了一个db的微指令，如果我们需要把他的长度类型进行改变，我们可以把鼠标放在db上，然后继续按住d进行修改，依次是db，dw，dd，dq（即byte，word，doubleword，quaterword）。

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

#### Ⅱ多数

如果我们需要一次性添加很多很多的变量，那么上面的方法就不可取了。

我们右键->array

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

可以看到这里为我们提供了批量创建变量的。

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

一般我们选择创建多个对象，并且为了便于修改名字，我们不把他设置为array类型，所以选择

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

创建后

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

他的批量创建的变量的长度是根据第一个对象的长度来的，默认是db。



### ③使用结构体

结构体创建好后，我们需要将他利用到我们的代码当中。

选择我们需要利用的变量，右键，选择convert to struct\*

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

然后我们可以看到里面有我们代码中所有的结构体，我们选择struct1，就是我们创建的那个。

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

然后我们可以得到

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

### ④修改完善结构体

我们可以看到我们的变量前面有很多的强制转换，因为我们在设置结构体的时候是所有的都是一个类型，这边检验最开始全部是db，因为我们对db足够熟悉。当然计算方式是一样的，我们修改的是结构体的结构，然后修改后可以得到

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

然后就是基本的修改它们的名字，改函数名之类的，简单的操作了。



## 2.带数组的结构体复原：

我们可以看到有一些时候会出现很规律的一些ptr+4，ptr+8，ptr+12之类的，或者我们会看到伪代码中出现for循环的，这种情况下就会有需要数组的结构体帮助我们学习。其实这也是修改结构体的一部分。

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

### ①创建数组

回到我们批量创建变量的页面

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

然后我们选择需要的数量，并且勾选的是Create ad array

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

然后就得到了数组变量

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

我们也可以在代码中看到这个地方有for循环，所以很直接的告诉我们需要变成数组

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

### ②利用数组











## 3.嵌套结构体复原：





















