---
show: step
version: 1.0
enable_checker: true
---

# 解码 decode

## 回忆上次内容

- code就是码
	- 最早也指电报码
	- 后来有各种编码、密码、砝码、条码
	- 都指的是把各种事物编个号
- encode就是编码
	- 编码就是给事物编个号

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663503862006)

- 编码基本了解了
	- 给事物编号就是编码
	- 怎么通过编号找到原来的事物呢？

### 解码

- 解码是编码的逆运算
	- 解铃换需系铃人


![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220911-1662869944064)

- 上次把白菜编上号
	- 这次扫到号知道是白菜
	- 扫到码就知道这个条码
	- 对应这个大白菜并知道价格

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220212-1644629532870)

- 这解码用英文怎么说呢？

### 解码(decode)

- de 的意思是相反的
	- defuse 解除保险炸弹引信
	- decolor 漂白
	- defame 中伤
	- destruct 破坏
	- demodulation 解调制
- decode 就是和 encode 相反的
	- 把一个代码还原为一个东西 

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220911-1662870240665)

- 我们的大脑在编码解码
	- 计算机也可以编码解码
- 我们用 python 试试解码

### 编解码

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210905-1630840207588)

- str(字符串)`'a'` encode(编码)之后 
	- 为 `b'\x61'`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220212-1644629638535)

- bytes(字节序列) `b'\x61'` decode(解码)之后
	- 得到str(字符串)`'a'`

- 编码(encode) 和解码(decode) 互为逆运算
- 很像
	- 字符(chr)和 序号(ord)
- 一阴一阳之谓道

### 编码解码

- 可以先编码再解码
- 也可以先解码再编码
- 绕来绕去
- 也没做神马😁

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210905-1630840380086)

- 掌握这个基础是最起码
- 基本功要练得硬桥硬马
- 实战方能稳扎稳打
- 否则以后各种乱码

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210917-1631860339560)

- 字节编码其实已经形成一个闭环

### 闭环

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221021-1666342050363)

- 字符的这三个东西形成了一个闭环
	- 字符本身
	- 字符序号数字
	- 字符的字节状态

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221021-1666342689996)

- 对一个字节可以解码为字符
- 对多个字节可以解码吗？

### 解码

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220924-1664024847442)

```
help(bytes.decode)
help(b"a".decode)
```

- 查询帮助手册

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220924-1664024944238)

- 不止字符串
- 任何进入计算机的东西都需要编码

### 图像编码

- 图像、声音、影片
	- 计算机中的一切都需要编码

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663504473731)

- 编码之后才能存储、传输
	- 还原的时候需要解码
	- 换一种编码方式叫做转码

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663504674762)

- 回到字符编码
	- ascii编码为什么这样编呢？
- 是乱编的吗？

### 大小字母差值


- 那么大小写字母之间有什么关系呢
	- `0x61-0x7A`这个范围是小写字母
	- `0x41-0x5A`这个范围是大写字母

```python
#输出a的ASCII码
ord("a")
#输出A的ASCII码
ord("A")
#输出大小写之差
ord("a")-ord("A")
#差值的16进制形式
hex(ord("a")-ord("A"))
#差值的2进制形式
bin(ord("a")-ord("A"))
```

- 大写字母和小写字母相差(`32`)<sub>`10进制`</sub>

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210220-1613809097080)

- 为什么不多不少
- 就差 (`32`)<sub>`10进制`</sub> 呢？
- 怎么那么寸呢？🤔
- 先去总结一下

### 总结

- decode
	- 就是解码
- 解码和编码可以转化
	- encode 编码
	- decode 解码
	- 互为逆过程
- 大小写字母之间序号全都相差(`32`)<sub>`10进制`</sub>

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221005-1664938405378)

- 这是为什么呢？🤔
- 我们下次再说👋🏻