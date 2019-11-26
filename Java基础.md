工具类
BeanUtils：https://blog.csdn.net/qidasheng2012/article/details/84562732
Maven依赖：
<dependency>
	<groupId>commons-beanutils</groupId>
	<artifactId>commons-beanutils</artifactId>
	<version>1.8.3</version>
</dependency>
常用API：
// 把orig对象copy到dest对象中.
public void copyProperties (Object dest, Object orig)
// 把Bean的属性值放入到一个Map里面
public Map describe(Object bean)
// 把map里面的值放入bean中
public void populate (Object bean, Map map)
// 设置Bean对象中名称为name的属性值赋值为value.	
public void setProperty(Object bean,String name, Object value)
// 取得bean对象中名为name的属性的值
public String getProperty(Object bean, String name)	


StringUtils：https://blog.csdn.net/qidasheng2012/article/details/83378431
Maven依赖：
<dependency>
	<groupId>org.apache.commons</groupId>
	<artifactId>commons-lang3</artifactId>
	<version>3.7</version>
</dependency>
常用API：
// 判断字符串是否为""或者null
public static boolean isEmpty(CharSequence cs)
// 跟上面方法相反
public static boolean isNotEmpty(CharSequence cs)
// 判断字符对象是不是空字符串，注意与isEmpty的区别
public static boolean isBlank(CharSequence cs)
// 和上一个方法相反
public static boolean isNotBlank(CharSequence cs)
// 移除字符串两端的空字符串
public static String trim(String str)
public static String trimToNull(String str)
public static String trimToEmpty(String str)
// 字符串比对方法，是比较实用的方法之一，两个比较的字符串都能为空，不会报空指针异常。
public static boolean equals(CharSequence cs1,  CharSequence cs2)
// 上面方法的变体, 字符串比较（忽略大小写），在验证码……等字符串比较，真是很实用。
public static boolean equalsIgnoreCase(CharSequence str1, CharSequence str2)
// indexOf这个方法不必多说，这个方法主要处理掉了空字符串的问题，不会报空指针，有一定用处
public static int indexOf(CharSequence seq, int searchChar)
// 字符串在另外一个字符串里，出现第Ordinal次的位置 
public static int ordinalIndexOf(CharSequence str, CharSequence searchStr, int ordinal)
// 字符串最后一次出现的位置
public static int lastIndexOf(CharSequence seq, int searchChar)
// 字符串seq是否包含searchChar
public static boolean contains(CharSequence seq, int searchChar)
// 包含后面数组中的任意对象，返回true
public static boolean containsAny(CharSequence cs, char... searchChars)
// 字符串截取 
public static String substring(String str, int start)
// 这三个方法类似都是截取字符串
public static String left(String str, int len)
public static String right(String str, int len)
public static String mid(String str, int pos, int len)
// 字符串分割 
public static String[] split(String str, String separatorChars
// 字符串连接
public static <T> String join(T... elements)
// 特定字符串连接数组，很多情况下还是蛮实用，不用自己取拼字符串 
public static String join(Object[] array, char separator)
// 删除空格
public static String deleteWhitespace(String str) 
// 删除以特定字符串开头的字符串，如果没有的话，就不删除。 
public static String removeStart(String str, String remove)
// 生成订单号，的时候还是很实用的。右边自动补齐。 
public static String rightPad(String str, int size, char padChar)
// 左边自动补齐 
public static String leftPad(String str, int size, char padChar)
// 将字符在某特定长度下，居中
public static String center(String str, int size)
// 首字母大写
public static String capitalize(String str)
// 反向大小写 
public static String swapCase(String str)
// 判断字符串是否由字母组成 
public static boolean isAlpha(CharSequence cs)
// 默认字符串，相当于三目运算，前面若为null，则返回后面一个参数 
public static String defaultString(String str, String defaultStr)
// 字符串翻转
public static String reverse(String str)
// 缩略字符串，省略号要占三位。maxWith小于3位会报错。
public static String abbreviate(String str, int maxWidth)
// 缩略字符串的一些高级用法 
public static String abbreviate(String str, int offset, int maxWidth)
// 包装，用后面的字符串对前面的字符串进行包装 
public static String wrap(String str, char wrapWith)





ArrayUtils：https://blog.csdn.net/qidasheng2012/article/details/83382796
Maven依赖：
<dependency>
	<groupId>org.apache.commons</groupId>
	<artifactId>commons-lang3</artifactId>
	<version>3.7</version>
</dependency>
常用API：
toString
将一个数组转换成String,用于打印数组
subarray
截取子数组
isSameLength
判断两个数组长度是否相等
getLength
获得数组的长度
isSameType
判段两个数组的类型是否相同
reverse
数组反转
indexOf
查询某个Object在数组中的位置,可以指定起始搜索位置
lastIndexOf
反向查询某个Object在数组中的位置,可以指定起始搜索位置
contains
查询某个Object是否在数组中
toObject
toPrimitive
基本数据类型数组与包装类数据类型数组互转
isEmpty
判断数组是否为空(null和length=0的时候都为空)
addAll
合并两个数组
add
添加一个数据到数组
remove
删除数组中某个位置上的数据
removeElement
删除数组中某个对象(从正序开始搜索,删除第一个)




接口类似问题

实现Serializable接口：
Serializable接口是Java的一个接口，一个类只有实现了该接口，其对象才能被序列化。
序列化是将一个对象及状态转化为可存储或者可传输的形式的过程，在序列化期间对象将其当前状态写入到临时存储区或者持久性存储区，之后便可以从存储区中读取或反序列化该对象的状态信息来重新创建该对象。
当我们需要把对象的状态信息持久保存或者通过网络传输时需要序列化，以便使用时进行反序列化。




理论概念
封装：将抽象性函式接口的实现细节包装，隐藏起来的方法，要访问该类的代码和数据，必须通过严格的接口控制。
封装最主要的功能在于我们能修改自己的实现代码，而不用修改那些调用我们代码的程序片段。适当封装可以让程式更容易理解与维护，也加强了代码安全性。
封装的优点：1.良好的封装可以减少耦合
			2.类内部的结构可以自由修改


