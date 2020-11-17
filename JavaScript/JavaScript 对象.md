# 一、array对象

1、concat()方法  连接两个或更多的数组，并返回结果。

*array1*.concat(*array2*,*array3*,...,*arrayX*)

返回一个新的数组。该数组是通过把所有 arrayX 参数添加到 arrayObject 中生成的。如果要进行 concat() 操作的参数是数组，那么添加的是数组中的元素，而不是数组。

2、copyWithin()方法 

从数组的指定位置拷贝元素到数组的另一个指定位置中。

![image-20200910170228515](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200910170228515.png)

3、entries方法 返回数组的可迭代对象

entries() 方法返回一个数组的迭代对象，该对象包含数组的键值对 (key/value)。

迭代对象中数组的索引值作为 key， 数组元素作为 value。

4、every()对象 检测数值元素的每个元素是否都符合条件

every() 方法用于检测数组所有元素是否都符合指定条件（通过函数提供）。

every() 方法使用指定函数检测数组中的所有元素：

- 如果数组中检测到有一个元素不满足，则整个表达式返回 *false* ，且剩余的元素不会再进行检测。
- 如果所有元素都满足条件，则返回 true。

**注意：** every() 不会对空数组进行检测， every() 不会改变原始数组。

![image-20200910172616075](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200910172616075.png)

5、fill()方法 用于将一个固定值替换数组的元素

![image-20200910173345831](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200910173345831.png)

6、filter()方法 检测数值元素，并返回符合条件所有元素的数组

注：filter()不会对空数组进行检测，不会改变原数组

![image-20200911100155741](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200911100155741.png)

7、find()方法  返回符合传入测试（函数）条件的数组元素

find() 方法返回通过测试（函数内判断）的数组的第一个元素的值。

find() 方法为数组中的每个元素都调用一次函数执行：

- 当数组中的元素在测试条件时返回 *true* 时, find() 返回符合条件的元素，之后的值不会再调用执行函数。
- 如果没有符合条件的元素返回 undefined

**注意:** find() 对于空数组，函数是不会执行的， find() 并没有改变数组的原始值。

![image-20200911101041793](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200911101041793.png)

8、findIndex() 返回符合传入测试(函数)条件的数组元素索引

findIndex() 方法返回传入一个测试条件（函数）符合条件的数组第一个元素位置。

findIndex() 方法为数组中的每个元素都调用一次函数执行：

- 当数组中的元素在测试条件时返回 *true* 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
- 如果没有符合条件的元素返回 -1

**注意:** findIndex() 对于空数组，函数是不会执行的， findIndex() 并没有改变数组的原始值。

![image-20200911101551664](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200911101551664.png)

9、forEach() 数组每个元素都执行一次回调函数

10、form() 通过给定的对象中创建一个数组

11、includes() 判断一个数组是否包含一个指定的值

12、indexOf() 判断数组中的元素，并返回它所在的位置

13、isArray() 判断对象是否为数组

14、join() 把数组的所有元素放入一个字符串

15、keys() 返回数组的可迭代对象，包含原始数组的键(key)

16、lastIndexOf() 搜索数组中的元素，并返回最后出现的位置

17、map()  通过指定函数处理数组的每个元素，并返回处理后的数组

18、pop() 删除数组的最后一个元素并返回删除的元素

19、push() 向数组的末尾添加一个或更多元素，并返回新的长度

20、reduce() 将数组元素计算为一个值(从左到右)

21、reduceRight() 将数组元素计算为一个值(从左到右)

22、reverse() 翻转数组的元素顺序 

23、shift()   删除并返回数组的第一个元素

24、slice() 选取数组的一部分，并返回一个新数组

25、some() 检测数组元素中是否有元素符合指定条件

26、splice() 从数组中添加或删除元素

27、toString()  把数组转换为字符串，并返回结果

28、unshift() 向数组的开头添加一个或更多元素，并返回新的长度

29、valueOf() 返回数组对象的原始值                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          

# 二、date对象 new Date()

1、getDate() 从 Date 对象返回一个月中的某一天 (1 ~ 31)

2、getDay() 从 Date 对象返回一周中的某一天 (0 ~ 6)

3、getFullYear() 从Date对象以四位数字返回年份

4、getHours()  返回 Date 对象的小时 (0 ~ 23)

5、getMinutes()  返回 Date 对象的分钟 (0 ~ 59)

6、getMilliseconds 返回 Date 对象的毫秒(0 ~ 999)

7、getMonth()  从 Date 对象返回月份 (0 ~ 11)

8、getSeconds() 从 Date 对象返回秒数(0~59)

9、getTime()  返回 1970 年 1 月 1 日至今的毫秒数

10、getTimezoneOffset() 返回本地时间与格林威治标准时间 (GMT) 的分钟差

11、UTC 世界时间 格林尼治时间

12、parse方法：返回1970年1月1日午夜到指定日期的毫秒数

13、set方法 设置日期时间

# 三、string对象 new String

1、charAt() 返回在指定位置的字符

2、charCodeAt() 返回在指定位置的字符的Unicode编码

3、