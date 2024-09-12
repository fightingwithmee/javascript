

# JavaScript基础

# 1.1引入javacript的方式

>  内部引入：通过 `script` 标签包裹 JavaScript 代码

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212057690.png)

```javascript
<body>
  <!-- 内联形式：通过 script 标签包裹 JavaScript 代码 -->
  <script>
    alert('嗨，欢迎来传智播学习前端技术！')
  </script>
</body>
```

> 外部引入：一般将 JavaScript 代码写在独立的以 .js 结尾的文件中，然后通过 `script` 标签的 `src` 属性引入

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212058854.png)

```javascript
<body>
  <!-- 外部形式：通过 script 的 src 属性引入独立的 .js 文件 -->
  <script src="demo.js"></script>
</body>
```

> 如果 script 标签使用 src 属性引入了某 .js 文件，那么 标签的代码会被忽略！！！

```js
<body>
  <!-- 外部形式：通过 script 的 src 属性引入独立的 .js 文件 -->
  <script src="demo.js">
    // 此处的代码会被忽略掉！！！！
  	alert(666);  
  </script>
</body>
```

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212106611.png)

## 1.2注释和结束符

> 使用 `// ` 注释单行代码
>
> 使用 `/* */` 注释多行代码
>
> 在 JavaScript 中 `;` 代表一段代码的结束，多数情况下可以省略 `;` 使用回车（enter）替代
>
> **建议省略**

```js
<script>
    // 这种是单行注释的语法
    // 一次只能注释一行
    // 可以重复注释
    /*
    	更常见的多行注释是这种写法
    	在些可以任意换行
    	多少行都可以
      */
    document.write('嗨，欢迎来传智播学习前端技术！');
  </script>
```

## 1.3输入

> alert()弹框
>
> document.write()写在页面上
>
> console.log()输出控制台

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212117038.png)

## 1.4输入

> 向 `prompt()` 输入任意内容会以弹窗形式出现在浏览器中，一般提示用户输入一些内容

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212119986.png)

## 1.5JavaScript语句执行顺序

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212123616.png)

## 1.6字面量

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212124236.png)





## 1.7变量

> 1.变量的声明：关键字和变量名，先声明后使用
>
> 2.变量的赋值

```js
<script>
  // x 符号代表了 5 这个数值
  x = 5 
  //举例： 在 JavaScript 中使用变量可以将某个数据（数值）记录下来！
  // 将用户输入的内容保存在 num 这个变量（容器）中
  num = prompt('请输入一数字!')

  // 通过 num 变量（容器）将用户输入的内容输出出来
  alert(num)
  document.write(num)

  //let 变量名并赋值，将 18 这个数据存入了 age 这个“容器”中

  let age = 18
  
	
</script>
```

## 1.7.2关键字

> let 和 var声明变量的细节
>
> 1.let不允许重复声明，var可以

## 1.7.3变量命名规则

> 1. 只能是字母、数字、下划线、$，且不能能数字开头
> 2. 字母区分大小写，如 Age 和 age 是不同的变量
> 3. JavaScript 内部已占用于单词（关键字或保留字）不允许使用
> 4. 尽量保证变量具有一定的语义，见字知义

```js
 <script> 
    let age = 18 // 正确
    let age1 = 18 // 正确
    let _age = 18 // 正确

    // let 1age = 18; // 错误，不可以数字开头
    let $age = 18 // 正确
    let Age = 24 // 正确，它与小写的 age 是不同的变量
    // let let = 18; // 错误，let 是关键字
    let int = 123 // 不推荐，int 是保留字
  </script>
```

## 1.8常量

>  const 声明的变量称为“常量”
>
>  **使用场景**：当某个变量永远不会改变的时候，就可以使用 const 来声明，而不是let

```js
<script>
  const age = 20//可以
  age = 30//报错，age的值不能改变
</script>
```

## 1.9数据类型

> 整数、小数、正数、负数
>
> **typeof** 关键字检测数据类型： console.log(typeof age)

```js
 <script> 
    let score = 100 // 正整数
    let price = 12.345 // 小数
    let temperature = -40 // 负数

    document.write(typeof score) // 结果为 number
    document.write(typeof price) // 结果为 number
    document.write(typeof temperature) // 结果为 number
  </script>
```

## 1.9.1字符串类型

> 通过单引号（ `''`） 、双引号（ `""`）或反引号包裹的数据都叫字符串，单引号和双引号**没有本质上的区别**，**推荐使用单引号**。
>
> 注意事项：
>
> 1. 无论单引号或是双引号必须成对使用
> 2. 单引号/双引号可以互相嵌套，但是不以自已嵌套自已
> 3. 必要时可以使用**转义符** `\`，输出单引号或双引号

```js
  <script> 
    let user_name = '小明' // 使用单引号
    let gender = "男" // 使用双引号
    let str = '123' // 看上去是数字，但是用引号包裹了就成了字符串了
    let str1 = '' // 这种情况叫空字符串
		
    documeent.write(typeof user_name) // 结果为 string
    documeent.write(typeof gender) // 结果为 string
    documeent.write(typeof str) // 结果为 string
  </script>
```



### 1.9.2布尔类型

> 表示肯定或否定,有两个固定的值 `true` 和 `false`

```js
 <script> 
    //  pink老师帅不帅？回答 是 或 否
    let isCool = true // 是的，摔死了！
    isCool = false // 不，套马杆的汉子！

    document.write(typeof isCool) // 结果为 boolean
  </script>
```



### 1.9.3undefineed

> 未定义是比较特殊的类型，只有一个值 undefined，只声明变量，不赋值的情况下，变量的默认值为 undefined，一般很少【直接】为某个变量赋值为 undefined。

```js
<script> 
    // 只声明了变量，并末赋值
    let tmp;
    document.write(typeof tmp) // 结果为 undefined
  </script>
```

## 1.10类型转换之隐式转换

> 某些运算符被执行时，系统内部自动将数据类型进行转换，这种转换称为隐式转换

```js
 <script> 
    let num = 13 // 数值
    let num2 = '2' // 字符串

    // 结果为 132
    // 原因是将数值 num 转换成了字符串，相当于 '13'
    // 然后 + 将两个字符串拼接到了一起
    console.log(num + num2)

    // 结果为 11
    // 原因是将字符串 num2 转换成了数值，相当于 2
    // 然后数值 13 减去 数值 2
    console.log(num - num2)

    let a = prompt('请输入一个数字')
    let b = prompt('请再输入一个数字')

    alert(a + b);
  </script>
```

## 1.10.1数据转换之显示转换

> 编写程序时过度依靠系统内部的隐式转换是不严禁的，因为隐式转换规律并不清晰，大多是靠经验总结的规律。为了避免因隐式转换带来的问题，通常根逻辑需要对数据进行显示转换
>
> **Number**:通过 `Number` 显示转换成数值类型，当转换失败时结果为 `NaN`（Not a Number）即不是一个数字

```js
<script>
    let t = '12'
    let f = 8

    // 显式将字符串 12 转换成数值 12
    t = Number(t)

    // 检测转换后的类型
    // console.log(typeof t);
    console.log(t + f) // 结果为 20

    // 并不是所有的值都可以被转成数值类型
    let str = 'hello'
    // 将 hello 转成数值是不现实的，当无法转换成
    // 数值时，得到的结果为 NaN （Not a Number）
    console.log(Number(str))
  </script>
```

# 2.1算术运算符

| 运算符 | 作用                                                 |
| ------ | ---------------------------------------------------- |
| +      | 求和                                                 |
| -      | 求差                                                 |
| *      | 求积                                                 |
| /      | 求商                                                 |
| **%**  | 取模（取余数），开发中经常用于作为某个数字是否被整除 |

```js
// 算术运算符
console.log(1 + 2 * 3 / 2) //  4 
let num = 10
console.log(num + 10)  // 20
console.log(num + num)  // 20

// 1. 取模(取余数)  使用场景：  用来判断某个数是否能够被整除
console.log(4 % 2) //  0  
console.log(6 % 3) //  0
console.log(5 % 3) //  2
console.log(3 % 5) //  3

// 2. 注意事项 : 如果我们计算失败，则返回的结果是 NaN (not a number)
console.log('pink老师' - 2)
console.log('pink老师' * 2)
console.log('pink老师' + 2)   // pink老师2
```

## 2.2赋值运算符

> 赋值运算符：对变量进行赋值的运算符
>
> =     将等号右边的值赋予给左边, 要求左边必须是一个容器
>
> 自增：++在前和++在后在单独使用时二者并没有差别，而且一般开发中我们都是独立使用
>
> 自减：++在后（后缀式）我们会使用更多

| 运算符 | 作用     | 说明                       |
| ------ | -------- | -------------------------- |
| +=     | 加法赋值 |                            |
| -+     | 减法赋值 |                            |
| *=     | 乘法赋值 |                            |
| /=     | 除法赋值 |                            |
| %=     | 取余赋值 |                            |
| ++     | 自增     | 变量自身的值加1，例如: x++ |
| --     | 自减     | 变量自身的值减1，例如: x-- |

```js
<script>
let num = 1
// num = num + 1
// 采取赋值运算符
// num += 1
num += 3
console.log(num)


// let num = 10
    // num = num + 1
    // num += 1
    // // 1. 前置自增
    // let i = 1
    // ++i
    // console.log(i)

    // let i = 1
    // console.log(++i + 1)
    // 2. 后置自增
    // let i = 1
    // i++
    // console.log(i)
    // let i = 1
    // console.log(i++ + 1)

    // 了解 
    let i = 1
    console.log(i++ + ++i + i)
</script>
```

## 2.3比较运算符

| 运算符 | 作用                                   |
| ------ | -------------------------------------- |
| >      | 左边是否大于右边                       |
| <      | 左边是否小于右边                       |
| >=     | 左边是否大于或等于右边                 |
| <=     | 左边是否小于或等于右边                 |
| ===    | 左右两边是否`类型`和`值`都相等（重点） |
| ==     | 左右两边`值`是否相等                   |
| !=     | 左右值不相等                           |
| !==    | 左右两边是否不全等                     |

```js
<script>
  console.log(3 > 5)
  console.log(3 >= 3)
  console.log(2 == 2)
  // 比较运算符有隐式转换 把'2' 转换为 2  双等号 只判断值
  console.log(2 == '2')  // true
  // console.log(undefined === null)
  // === 全等 判断 值 和 数据类型都一样才行
  // 以后判断是否相等 请用 ===  
  console.log(2 === '2')
  console.log(NaN === NaN) // NaN 不等于任何人，包括他自己
  console.log(2 !== '2')  // true  
  console.log(2 != '2') // false 
  console.log('-------------------------')
  console.log('a' < 'b') // true
  console.log('aa' < 'ab') // true
  console.log('aa' < 'aac') // true
  console.log('-------------------------')
</script>
```

## 2.4逻辑运算符

| 符号 | 名称   | 日常读法 | 特点                       | 口诀           |
| ---- | ------ | -------- | -------------------------- | -------------- |
| &&   | 逻辑与 | 并且     | 符号两边有一个假的结果为假 | 一假则假       |
| \|\| | 逻辑或 | 或者     | 符号两边有一个真的结果为真 | 一真则真       |
| !    | 逻辑非 | 取反     | true变false  false变true   | 真变假，假变真 |

| A     | B     | A && B | A \|\| B | !A    |
| ----- | ----- | ------ | -------- | ----- |
| false | false | false  | false    | true  |
| false | true  | false  | true     | true  |
| true  | false | false  | true     | false |
| true  | true  | true   | true     | false |

```js
<script>
    // 逻辑与 一假则假
    console.log(true && true)
    console.log(false && true)
    console.log(3 < 5 && 3 > 2)
    console.log(3 < 5 && 3 < 2)
    console.log('-----------------')
    // 逻辑或 一真则真
    console.log(true || true)
    console.log(false || true)
    console.log(false || false)
    console.log('-----------------')
    // 逻辑非  取反
    console.log(!true)
    console.log(!false)

    console.log('-----------------')

    let num = 6
    console.log(num > 5 && num < 10)
    console.log('-----------------')
  </script>
```

## 2.5运算符优先级

> 逻辑运算符优先级： ！> && >  ||  

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212152021.png)

# 3.1表达式和语句

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212157439.png)

## 3.2分支语句

> 1. if分支语句（重点）
> 2. 三元运算符
> 3. switch语句

### 3.2.1 if分支语句

```js
if(条件表达式) {
  // 满足条件要执行的语句
}
```

## 3.2.2 if双分支语句

```js
if (条件表达式){
  // 满足条件要执行的语句
} else {
  // 不满足条件要执行的语句
}

 <script>
    // 1. 用户输入
    let uname = prompt('请输入用户名:')
    let pwd = prompt('请输入密码:')
    // 2. 判断输出
    if (uname === 'pink' && pwd === '123456') {
      alert('恭喜登录成功')
    } else {
      alert('用户名或者密码错误')
    }
  </script>

```

### 3.2.3if 多分支语句

```js
 <script>
    // 1. 用户输入
    let score = +prompt('请输入成绩：')
    // 2. 判断输出
    if (score >= 90) {
      alert('成绩优秀，宝贝，你是我的骄傲')
    } else if (score >= 70) {
      alert('成绩良好，宝贝，你要加油哦~~')
    } else if (score >= 60) {
      alert('成绩及格，宝贝，你很危险~')
    } else {
      alert('成绩不及格，宝贝，我不想和你说话，我只想用鞭子和你说话~')
    }
  </script>
```

### 3.2.4三元运算符（三元表达式）

> 条件 ? 表达式1 ： 表达式2

```js
<script>
// 三元运算符（三元表达式）
// 1. 语法格式
// 条件 ? 表达式1 : 表达式2 

// 2. 执行过程 
// 2.1 如果条件为真，则执行表达式1
// 2.2 如果条件为假，则执行表达式2

// 3. 验证
// 5 > 3 ? '真的' : '假的'
console.log(5 < 3 ? '真的' : '假的')
</script>
```

## 3.3switch语句

> 1. switch case语句一般用于等值判断, if适合于区间判断
> 2. switchcase一般需要配合break关键字使用 没有break会造成case穿透
> 3. if 多分支语句开发要比switch更重要，使用也更多

```js
// switch分支语句
// 1. 语法
// switch (表达式) {
//   case 值1:
//     代码1
//     break

//   case 值2:
//     代码2
//     break
//   ...
//   default:
//     代码n
// }

<script>
  switch (2) {
    case 1:
    console.log('您选择的是1')
    break  // 退出switch
    case 2:
    console.log('您选择的是2')
    break  // 退出switch
    case 3:
    console.log('您选择的是3')
    break  // 退出switch
    default:
    console.log('没有符合条件的')
  }
</script>
```

## 3.4while循环

> while :  在…. 期间， 所以 while循环 就是在满足条件期间，重复执行某些代码
>
> 循环三要素：
>
> 1.初始值 （经常用变量）
>
> 2.终止条件
>
> 3.变量的变化量

```js
// while循环: 重复执行代码

let i = 1 //变量的起始值
while (i <= 3) { //终止条件
  document.write(i)
  i++   // 变量的变化量
}
```

## 3.5中止循环

> `break`   中止整个循环，一般用于结果已经得到, 后续的循环不需要的时候可以使用（提高效率）  
>
> `continue`  中止本次循环，一般用于排除或者跳过某一个选项的时候

```js
<script>
    // let i = 1
    // while (i <= 5) {
    //   console.log(i)
    //   if (i === 3) {
    //     break  // 退出循环
    //   }
    //   i++

    // }


    let i = 1
    while (i <= 5) {
      if (i === 3) {
        i++
        continue
      }
      console.log(i)
      i++

    }
  </script>
```

## 3.6无限循环

> 1.while(true) 来构造“无限”循环，需要使用break退出循环。（常用）
>
> 2.for(;;) 也可以来构造“无限”循环，同样需要使用break退出循环。

```js
// 无限循环  
// 需求： 页面会一直弹窗询问你爱我吗？
// (1). 如果用户输入的是 '爱'，则退出弹窗
// (2). 否则一直弹窗询问

// 1. while(true) 无限循环
// while (true) {
//   let love = prompt('你爱我吗?')
//   if (love === '爱') {
//     break
//   }
// }

// 2. for(;;) 无限循环
for (; ;) {
  let love = prompt('你爱我吗?')
  if (love === '爱') {
    break
  }
}
```

## 3.7for 语句

```js
<script>
  // 1. 语法格式
  // for(起始值; 终止条件; 变化量) {
  //   // 要重复执行的代码
  // }

  // 2. 示例：在网页中输入标题标签
  // 起始值为 1
  // 变化量 i++
  // 终止条件 i <= 6
  for(let i = 1; i <= 6; i++) {
    document.write(`<h${i}>循环控制，即重复执行<h${i}>`)
  }
</script>


<script>
    // 1. continue 
    for (let i = 1; i <= 5; i++) {
        if (i === 3) {
            continue  // 结束本次循环，继续下一次循环
        }
        console.log(i)
    }
    // 2. break
    for (let i = 1; i <= 5; i++) {
        if (i === 3) {
            break  // 退出结束整个循环
        }
        console.log(i)
    }
</script>
```

## 3.8嵌套循环

```js
// 1. 外面的循环 记录第n天 
for (let i = 1; i < 4; i++) {
    document.write(`第${i}天 <br>`)
    // 2. 里层的循环记录 几个单词
    for (let j = 1; j < 6; j++) {
        document.write(`记住第${j}个单词<br>`)
    }
}
```



## 3.9断点调试

**作用：**学习时可以帮助更好的理解代码运行，工作时可以更快找到bug

浏览器打开调试界面

1. 按F12打开开发者工具
2. 点到源代码一栏 （ sources ）
3. 选择代码文件

**断点：**在某句代码上加的标记就叫断点，当程序执行到这句有标记的代码时会暂停下来

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212210324.png)

# 4.1定义数组

> Array是一种可以按顺序保存数据的数据类型

```js
<script>
  // 1. 语法，使用 [] 来定义一个空数组
  // 定义一个空数组，然后赋值给变量 classes
  // let classes = [];

  // 2. 定义非空数组
  let classes = ['小明', '小刚', '小红', '小丽', '小米']
</script>
```

## 4.2访问数组

```js
<script>
  let classes = ['小明', '小刚', '小红', '小丽', '小米']
  
  // 1. 访问数组，语法格式为：变量名[索引值]
  document.write(classes[0]) // 结果为：小明
  document.write(classes[1]) // 结果为：小刚
  document.write(classes[4]) // 结果为：小米
  
  // 2. 通过索引值还可以为数组单重新赋值
  document.write(classes[3]) // 结果为：小丽
  // 重新为索引值为 3 的单元赋值
  classes[3] = '小小丽'
  document.wirte(classes[3]); // 结果为： 小小丽
</script>
```

## 4.3数据单元值类型

```js
<script>
  // 6. 数组单值类型可以是任意数据类型

  // a) 数组单元值的类型为字符类型
  let list = ['HTML', 'CSS', 'JavaScript']
  // b) 数组单元值的类型为数值类型
  let scores = [78, 84, 70, 62, 75]
  // c) 混合多种类型
  let mixin = [true, 1, false, 'hello']
</script>
```

## 4.4数组长度属性

```js
<script>
  // 定义一个数组
  let arr = ['html', 'css', 'javascript']
  // 数组对应着一个 length 属性，它的含义是获取数组的长度
  console.log(arr.length) // 3
</script>
```

## 4.5操作数组

> 1. push 动态向数组的尾部添加一个单元
> 2. unshit 动态向数组头部添加一个单元
> 3. pop 删除最后一个单元
> 4. shift 删除第一个单元
> 5. splice 动态删除任意单元

```js
<script>
  // 定义一个数组
  let arr = ['html', 'css', 'javascript']

  // 1. push 动态向数组的尾部添加一个单元
  arr.push('Nodejs')
  console.log(arr)// ['html', 'css', 'javascript','Node.js']
  arr.push('Vue')// ['html', 'css', 'javascript','Node.js','Vue']

  // 2. unshit 动态向数组头部添加一个单元
  arr.unshift('VS Code')
  console.log(arr)// ['Vs Code',html', 'css', ...]

  // 3. splice 动态删除任意单元
  arr.splice(2, 1) // 从索引值为2的位置开始删除1个单元
  console.log(arr)

  // 4. pop 删除最后一个单元
  arr.pop()
  console.log(arr)

  // 5. shift 删除第一个单元
  arr.shift()
  console.log(arr)
</script>
```



# 5.1函数

> 和变量命名基本一致
>
> 小驼峰命名法

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212247617.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212247038.png)

```js
  <script>
    // 声明（定义）了最简单的函数，既没有形式参数，也没有返回值
    function sayHi() {
      console.log('嗨~')
    }
    // 函数调用，这些函数体内的代码逻辑会被执行
    // 函数名()
        
    sayHi()
    // 可以重复被调用，多少次都可以
    sayHi()
  </script>
```

## 5.2参数

> 通过向函数传递参数，可以让函数更加灵活多变，参数可以理解成是一个变量。
>
> 声明（定义）一个功能为打招呼的函数
>
> - 传入数据列表
> - 声明这个函数需要传入几个数据
> - 多个数据用逗号隔开

```js
  <script>
    // 声明（定义）一个功能为打招呼的函数
    // function sayHi() {
    //   console.log('嗨~')
    // }
    // 调用函数
    // sayHi()
	

    // 这个函数似乎没有什么价值，除非能够向不同的人打招呼
    // 这就需要借助参数来实现了
    function sayHi(name) {
      // 参数 name 可以被理解成是一个变量
      console.log(name)
      console.log('嗨~' + name)
    }

    // 调用 sayHi 函数，括号中多了 '小明'
    // 这时相当于为参数 name 赋值了
    sayHi('小明')// 结果为 小明

    // 再次调用 sayHi 函数，括号中多了 '小红'
    // 这时相当于为参数 name 赋值了
    sayHi('小红') // 结果为 小红
  </script>
```

## 5.3形参和实参

> 形参：声明函数时写在函数名右边小括号里的叫形参（形式上的参数）
>
> 实参：调用函数时写在函数名右边小括号里的叫实参（实际上的参数）
>
> 形参可以理解为是在这个函数内声明的变量（比如 num1 = 10）实参可以理解为是给这个变量赋值

```js
<script>
    // 声明（定义）一个计算任意两数字和的函数
    // 形参 x 和 y 分别表示任意两个数字，它们是两个变量
    function count(x, y) {
      console.log(x + y);
    }
    // 调用函数，传入两个具体的数字做为实参
    // 此时 10 赋值给了形参 x
    // 此时 5  赋值给了形参 y
    count(10, 5); // 结果为 15
  </script>
```

## 5.4返回值

> 函数的本质是封装（包裹），函数体内的逻辑执行完毕后，函数外部如何获得函数内部的执行结果呢？要想获得函数内部逻辑的执行结果，需要通过 `return` 这个关键字，将内部执行结果传递到函数外部，这个被传递到外部的结果就是返回值。

```js
  <script>
    // 定义求和函数
    function count(a, b) {
      let s = a + b
      // s 即为 a + b 的结果
      // 通过 return 将 s 传递到外部
      return s
    }

    // 调用函数，如果一个函数有返回值
    // 那么可将这个返回值赋值给外部的任意变量
    let total = count(5, 12)
  </script>
```

## 5.5作用域

> 全局作用域
>
> 作用于所有代码执行的环境(整个 **script 标签内部**)或者一个独立的 js 文件
>
> 处于全局作用域内的变量，称为全局变量
>
> 局部作用域
>
> 作用于**函数内的代码**环境，就是局部作用域。 因为跟函数有关系，所以也称为函数作用域。
>
> 处于局部作用域内的变量称为局部变量

```js
<script>
    let age = 30//全局作用域
    function a() {
        let num = 20//局部变量
        console.log(num)//就近原则
    }
</script>

```

## 5.6函数访问原则

## ![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212259524.png)5.7匿名函数的函数表达式

> 没有名字的函数,无法直接使用
>
> **函数表达式**：将匿名函数赋值给以恶变量，并且通过变量名称进行调用

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212302334.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212303025.png)

```js
<script>
    // 声明
    let fn = function() {
        console.log('函数表达式')
    }
    // 调用
    fn()
	//函数表达式传参
	let fn = function(x, y){
        console.log(x + y)
    }
    fn(1,2)
	//具名函数
	function fun(){
        console.log(1)
    }
	fun()
	

</script>
```

## 5.7箭头函数

![](https://raw.githubusercontent.com/fightingwithmee/vue/main/img/202312122127430.png)

![](https://raw.githubusercontent.com/fightingwithmee/vue/main/img/202312122152439.png)

![](https://raw.githubusercontent.com/fightingwithmee/vue/main/img/202312122151915.png)







![](https://raw.githubusercontent.com/fightingwithmee/vue/main/img/202312122152512.png)

```vue
<script>
    //普通函数
	function 函数名(){
        函数体
    }
    function sayHi(){
        console.log("123")
    }
    //函数表达式/匿名函数
    const fn = function(){//把函数赋给了fn
        console.log("123")
    }
    //调用
    fn()
    //箭头函数
    const fn = () => {
        console.log(123);
    }
    //调用
    fn()
    //只有一个形参的时候，可以省略小括号
    const fn = x => {
        console.log(x)
    }
    fn(1)
</script>
```



```vue
<script>
    //只有一行代码的时候，我们可以省略大括号
    const fn = x => console.log(x)
 	//只有一行代码的时候，可以省略return
    //1.1
    const fn = x => {
        return x + x
    } 
    //1.2和1.1一样
    const fn = x => x + x
    console.log(fn(1))
    //箭头函数可以直接返回一个对象
    const fn = (uname) => ({uname:uname})//因为函数包着的是大括号，函数体也是大括号，冲突了所以换成小括号
    console.log( fn("刘德华") );
</script>
```

## 5.87立刻执行函数

> (function(){})函数体
>
> ()执行函数

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212309725.png)

```js
<script>

    (function(){ xxx  })();

    (function (){console.log(11)})()

    (function(){xxxx}());

</script>

```

# 6.0对象

> 声明一个对象类型的变量与之前声明一个数值或字符串类型的变量没有本质上的区别

```js
 <script>
    // 声明字符串类型变量
    let str = 'hello world!'
    
    // 声明数值类型变量
    let num = 199

    // 声明对象类型变量，使用一对花括号
    // user 便是一个对象了，目前它是一个空对象
    let user = {}
  </script>
```

## 6.1属性

> 数据描述性的信息称为属性，如人的姓名、身高、年龄、性别等，一般是名词性的。
>
> 1. 属性都是成 对出现的，包括属性名和值，它们之间使用英文 `:` 分隔
> 2. 多个属性之间使用英文 `,` 分隔
> 3. 属性就是依附在对象上的变量
> 4. 属性名可以使用 `""` 或 `''`，一般情况下省略，除非名称遇到特殊符号如空格、中横线等

```js
 <script>
    // 通过对象描述一个人的数据信息
    // person 是一个对象，它包含了一个属性 name
    // 属性都是成对出现的，属性名 和 值，它们之间使用英文 : 分隔
    let person = {
      name: '小明', // 描述人的姓名
      age: 18, // 描述人的年龄
      stature: 185, // 描述人的身高
      gender: '男', // 描述人的性别
    }
  </script>
```

## 6.2属性访问

> 声明对象，并添加了若干属性后，可以使用 `.` 或 `[]` 获得对象中属性对应的值

```js
  <script>
    // 通过对象描述一个人的数据信息
    // person 是一个对象，它包含了一个属性 name
    // 属性都是成对出现的，属性名 和 值，它们之间使用英文 : 分隔
    let person = {
      name: '小明', // 描述人的姓名
      age: 18, // 描述人的年龄
      stature: 185, // 描述人的身高
      gender: '男', // 描述人的性别
    };
    
    // 访问人的名字
    console.log(person.name) // 结果为 小明
    // 访问人性别
    console.log(person.gender) // 结果为 男
    // 访问人的身高
    console.log(person['stature']) // 结果为 185
   // 或者
    console.log(person.stature) // 结果同为 185
  </script>
```

## 6.3动态为对象添加属性

```js
 <script>
    // 声明一个空的对象（没有任何属性）
	let user = {}
    // 动态追加属性
    user.name = '小明'
    user['age'] = 18
    
    // 动态添加与直接定义是一样的，只是语法上更灵活
  </script>
```

## 6.4方法和调用

> 数据行为性的信息称为方法，如跑步、唱歌等，一般是动词性的，其本质是函数。
>
> 1. 方法是由方法名和函数两部分构成，它们之间使用 : 分隔
> 2. 多个属性之间使用英文 `,` 分隔
> 3. 方法是依附在对象中的函数
> 4. 方法名可以使用 `""` 或 `''`，一般情况下省略，除非名称遇到特殊符号如空格、中横线等

```js
<script>
    // 方法是依附在对象上的函数
    let person = {
      name: '小红',
      age: 18,
      // 方法是由方法名和函数两部分构成，它们之间使用 : 分隔
      singing: function () {
        console.log('两只老虎，两只老虎，跑的快，跑的快...')
      },
      run: function () {
        console.log('我跑的非常快...')
      }
      // 调用对象中 singing 方法
      person.singing()
      // 调用对象中的 run 方法
      person.run()
    }
  </script>
```

## 6.5动态为对象添加方法

```js
  <script>
    // 声明一个空的对象（没有任何属性，也没有任何方法）
	let user = {}
    // 动态追加属性
    user.name = '小明'
    user.['age'] = 18
    
    // 动态添加方法
    user.move = function () {
      console.log('移动一点距离...')
    }
    
  </script>
```

## 6.6null

null 也是 JavaScript 中数据类型的一种，通常只用它来表示不存在的对象。使用 typeof 检测类型它的类型时，结果为 `object`。

## 6.7遍历对象

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312212323314.png)

```js
let obj = {
    uname: 'pink'
}
for(let k in obj) {
    // k 属性名  字符串  带引号    obj.'uname'     k ===  'uname'
    // obj[k]  属性值    obj['uname']   obj[k]
}

<script>
    let arr = ['pink','red','blue']
    for(let k in arr){
        console.log(k)//数组的下标 索引号 但是是字符串 '0'
        console.log(arr[k])
    }
	
	let obj = {
    uname: 'pink'
	}
	for(let k in obj) {
    // k 属性名  字符串  带引号    obj.'uname'     k ===  'uname'
    // obj[k]  属性值    obj['uname']   obj[k]
	}
	
</script>

```

```js
let obj = {
        username: 'pink老师',
        age: 18,
        gender: '男'
    }
    //for in 遍历对象
    for (let k in obj) {
        console.log(k)//属性名 显示的是'uname' 'age' 'gender'
        console.log(obj.k)
        console.log(obj['uname'])
    }
```

## 6.8内置对象

```
// 圆周率
console.log(Math.PI);
// 0 ~ 1 之间的随机数, 包含 0 不包含 1
Math.random()
// 舍弃小数部分，整数部分加1
Math.ceil(3.4)
// 舍弃小数部分，整数部分不变
Math.floor(4.68)
// 取整，四舍五入原则
Math.round(5.46539)
Math.round(4.849)
// 找出最大值
Math.max(10, 21, 7, 24, 13)
// 找出最小值
Math.min(24, 18, 6, 19, 21)
// 求某个数的多少次方
Math.pow(4, 2) // 求 4 的 2 次方
Math.pow(2, 3) // 求 2 的 3 次方
// 求某数的平方根
Math.sqrt(16)
```

# 6.9Const

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220004245.png)

```js
<script>
    const arr = ['red','pink']//const arr的意思是arr的地址不能变，元素插入数组和删除不该				   变他的地址
    arr.push('blue')
	arr = [1,2,3]//这就是arr改变地址了
    console.log(arr)
</script>
```

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220003725.png)

# 7.1Dom作用和分类

> dom就是用来操作网页的

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220023724.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220025882.png)

## 7.1Dom树

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220029372.png)

## 7.2Dom对象

> 在html叫标签，在js里面叫对象
>
> document对象就是整个页面
>
> 所有元素都在document里面

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220041374.png)

```js
<div>123</div>
<script>
    const div = document.querySelector('div');
    //打印对象
    console.dir(div)
    console.log(div)//<div>123</div>
</script>
</body>
```

## 7.3获取Dom元素

> 查找元素DOM元素就是利用JS选择页面中标签元素
>
> 1. querySelector   满足条件的第一个元素
> 2. querySelectorAll  满足条件的元素集合 返回伪数组
> 3. 了解其他方式
>    1. getElementById
>    2. getElementsByTagName

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220103479.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220104933.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220112852.png)

```js
<div class="box"></div>
<p id="nav">导航栏</p>
<ul>
    <li>测试1</li>
    <li>测试2</li>
    <li>测试3</li>
</ul>
<script>
    //1.获取匹配的第一个元素
    // const box = document.querySelector('div');
    // const box = document.querySelector('.box');
    // console.log(box)
    // const nav = document.querySelector('#nav');
    // console.log(nav)
    //2.获取第一个小li
    // const li = document.querySelector('ul li:first-child');
    // console.log(li)
    //3.选择所有小li
    const lis = document.querySelectorAll('ul li');
    //console.log(lis)
	for (let i = 0; i < lis.length; i++) {
        console.log(lis[i])//每个小li的对象
    }
</script>
```

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312220113791.png)

## 7.4操作元素内容

> DOM对象都是根据标签生成的,所以操作标签,本质上就是操作DOM对象
>
> 对象.innerText属性:将文本内容跟新到任意标签位置，**显示纯文本，不解析标签**
>
> 对象.innerHTML属性: **解析标签**，多标签使用模板字符

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221349695.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221353434.png)

```js
<div class="box">我是文字内容</div>
<script>
    //1.获取元素内容
    const box = document.querySelector(".box");
    console.log(box.innerText)//我是文字内容
    //2.修改文字内容 对象.innerText属性
    // box.innerText = '<h1>hello world</h1>'//不解析标签内容
    box.innerText = 'hello world'
	//3. innerHTML 解析标签
    box.innerHTML = '<h1>我要更换</h1>'
</script>

```

## 7.4操作元素属性

> 对象.属性 = 值
>
> 常见属性：herf、title、src

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221358599.png)

```js
<img src="./assets/01.jpg">
<script>
        //1.获取图片元素
        const img = document.querySelector("img");
        //2.修改图片对象的属性   对象.属性 = 值
        img.src = './assets/02.jpg'
        img.title = 'hello world'
</script>
```

## 7.5.1操作classList操作类控制CSS

> classList方式追加和删除类名

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221440353.png)

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box{
            width: 200px;
            height: 200px;
            background-color: red;
        }
        .active{
            color: blue;
            background-color: pink;
        }
    </style>
</head>
<body>
<div class="box">文字</div>

<script>
    //1.获取元素
    const box = document.querySelector(".box")
    //2修改样式
    //2.1 追加类add() 类名不加点，并且是字符串
    // box.classList.add('active')
    //2.2 删除类 remove() 类名不加点，并且是字符串
    // box.classList.remove("box")
    //2.3 切换类 toggle() 有就删没有就加上
    box.classList.toggle("active")

</script>

</body>
</html>
```



### 7.5.2操作style修改CSS

> 对象.style.样式属性 = 值

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221410497.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221417509.png)

```js
<body>
<div class="box"></div>
<script>
    //1.获取元素
    const box = document.querySelector('.box');
    //2.修改样式属性 对象.style.样式属性 = '值'
    box.style.width = '500px'
    //3.多组单词的采取 小驼峰命名法
    box.style.backgroundColor = 'skyblue'
    box.style.border = '2px solid blue'
    box.style.borderTop = '2px solid red'
</script>
</body>
```

### 7.5.3操作类名className操作CSS

> 元素.className = 'active'

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221425366.png)

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .box {
            width: 300px;
            height: 300px;
            background-color: skyblue;
            margin: 100px auto;
            padding: 10px;
            border: 1px solid #000;
        }
    </style>
</head>
<body>
<div class="nav"></div>
<script>
    //1.获取元素
    const div = document.querySelector('div');
    //2.单独给div添加类名 class是个关键子 用className
    div.className = 'box'
    // div.className = 'nav box'//加两个类名 nav 和 box

</script>
</body>
</html>
```

## 7.6操作表单元素 属性

> 获取：DOM对象.属性名
>
> 设置：DOM对象.属性名= 新值
>
> **获取值 获取表单里面的值 表单.value**

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221443104.png)

```js
<input type="text" value="电脑">
<script>
    //1.获取元素
    const uname = document.querySelector('input');
    //2.获取值 获取表单里面的值 表单.value
    // console.log(uname.value)//电脑
    // console.log(uname.innerHTML) //innerHTML 得不到表单内容
    //3.设置表单的值
    // uname.value = 'hello world'
    uname.type = 'password'
</script>

```

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221501767.png)

```js
<input type="checkbox" name="" id="" >
<button disabled>点击</button>
<script>
    //1.获取
    const ipt = document.querySelector('input');
    // console.log(ipt.checked)//false
    ipt.checked = true
    console.log('============')
    //1.获取
    const btn = document.querySelector('button');
    // console.log(btn.disabled)//默认false不禁用
    btn.disabled = false
</script>
```

## 7.7自定义属性

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221510673.png)

```js
    <div data-id="1" data-spm="不知道">1</div>
    <div data-id="2">2</div>
    <div data-id="3">3</div>
    <div data-id="4">4</div>
    <div data-id="5">5</div>
    <script>
        const div = document.querySelector('div');
        console.log(div.dataset.id) // 1
        console.log(div.dataset.spm) // 不知道
    </script>
```



## 7.8定时器-间隙函数

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221522205.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221529037.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221615239.png)

```js
<script>
    // setInterval(function (){
    //     console.log("你好")
    // },2000)
    function fn(){
        console.log("你好")
    }
    const n = setInterval(fn,2000)
    console.log(n)
    clearInterval(n)
</script>
```

# 8.0事件监听

> 元素对象.addEventListener('事件类型'，要执行的函数)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221639507.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221640643.png)

```js
<button>点击</button>
<script>
    // 1. 获取 button 对应的 DOM 对象
    const btn = document.querySelector('button');
    // 2. 添加事件监听
    btn.addEventListener('click',()=>{
        alert("hello world")
    })
</script>
```

## 8.1事件类型

> click:鼠标点击
>
> mouseenter:鼠标经过
>
> mouseleave:鼠标离开
>
> focus:获得焦点
>
> blur:市区焦点
>
> keydown:键盘按下触发
>
> keyup:键盘抬起触发
>
> input:用户输入事件

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221708663.png)

```js
<div></div>
<input type="text">
<script>
    const div = document.querySelector('div');
    div.addEventListener('mouseleave',()=>{
        // div.style.display = 'none'
        console.log("我走了")
    })
    div.addEventListener('mouseenter',()=>{
        // div.style.display = 'none'
        console.log("我来了")
    })
    const ipt = document.querySelector('input');
    ipt.addEventListener('focus',()=>{
        console.log("获得焦点")
    })

</script>
```

```js
<input type="text">
<script>
const ipt = document.querySelector('input');
    ipt.addEventListener('keydown',()=>{
        console.log("键盘摁下了")
    })
</script>
```

```js
<input type="text">
<script>
const ipt = document.querySelector('input');
     ipt.addEventListener('focus',()=>{
        console.log("获得焦点")
     })
</script>
```

```js
<input type="text">
<script>
    const input = document.querySelector('input');
    input.addEventListener('input',()=>{
        console.log(123)
    })
</script>
```


```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .a {
            width: 500px;
            height: 200px;
            margin: 0 auto;
            text-align: center;
            background-color: pink;
        }
        .x {
            width: 10px;
            height: 10px;
            margin-left: 470px;
            margin-top: -60px;
            background-color: skyblue;
        }
    </style>
</head>
<body>
<div class="box">
    <h1>我是广告</h1>
    <button class="down">x</button>
</div>

<script>
    const box = document.querySelector('.a');
    const down = document.querySelector('.x');
    down.addEventListener('click',()=>{
        box.style.display = 'none'
    })
</script>
</body>
</html>
```

## 8.1获取事件对象

> event，ev，e

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221819789.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221820862.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221823164.png)

```js
<input type="text">
<script>
    const btn = document.querySelector('input');
    btn.addEventListener('keyup',(e)=>{
        // console.log(e)
        console.log(e.key)
    })
</script>
```

## 8.2环境对象

> **谁调用，this就指向谁**

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221836232.png)

```js
<button>点击</button>
<script>
    //每个函数里面都有this 环境对象 普通函数里面this指向的是window
    // function fn(){
    //     console.log(this)//指向window，因为是window调用他
    // }
    // window.fn()
    const btn = document.querySelector('button');
    btn.addEventListener('click',function (){
        console.log(this)//指向button，因为是button调用的
        // btn.style.color = 'red'
        this.style.color = 'red'

    })


</script>
```

## 8.3回调函数

> 函数A当作参数传递给函数B，A就叫回调函数

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312221840059.png)

# 9.0事件流

> 事件完整执行过程中的流动路径
>
> **冒泡：子到父**
>
> 捕获：父到子

## 9.1捕获

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222125397.png)

## 9.2冒泡

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222127561.png)

```js
<div class="father">
    <div class="son"></div>
</div>

<script>

    const father = document.querySelector('.father');
    const son = document.querySelector('.son');
    father.addEventListener('click',()=>{
       alert("爸爸")
    })
    son.addEventListener('click',()=>{
        alert("儿子")
    })

    document.addEventListener('click',function (){
        alert("我是爷爷")
    })
</script>
```

## 9.3阻止冒泡

> 事件对象.stopPropagation()
>
> 鼠标经过事件：
>
> mouseover 和 mouseout 会有冒泡效果
>
> **mouseenter  和 mouseleave   没有冒泡效果 (推荐)**

```js
<div class="father">
    <div class="son"></div>
</div>

<script>

    const father = document.querySelector('.father');
    const son = document.querySelector('.son');
    son.addEventListener('click',(e)=>{
        e.stopPropagation()
        alert("儿子")

    })
    father.addEventListener('click',()=>{
       alert("爸爸")
    })


    document.addEventListener('click',function (){

        alert("我是爷爷")
    })
</script>
```

## 9.4解绑事件

> addEventListener方式用removeEventListener('click',fn)
>
> onclick:直接用null覆盖偶就可以实现事件的解绑

```js
//第一种
<button>点击</button>
<script>

    function fn(){
        alert("点击了")
    }
    const btn = document.querySelector('button');
    btn.addEventListener('click',fn)
    btn.removeEventListener('click',fn)

</script>
```

```js
//第二种方式onclick
btn.onclick = function(){
 alert('点击了')
}
//解绑
btn.onclick = null
```

## 9.5事件委托

> 事件的的冒泡模式总是会将事件流向其父元素的，如果父元素监听了相同的事件类型，那么父元素的事件就会被触发并执行

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222142216.png)

```js
<script>
  // 假设页面中有 10000 个 button 元素
  const buttons = document.querySelectorAll('table button')
  
  // 假设上述的 10000 个 buttom 元素共同的祖先元素是 table
  const parents = document.querySelector('table')
  parents.addEventListener('click', function (e) {
    // console.log(ev.target);
    // 只有 button 元素才会真正去执行逻辑
    if(e.target.tagName === 'BUTTON') {
      // 执行的逻辑
    }
  })
</script>
```

## 9.6阻止默认行为

> 防止链接的跳转，表单域跳转
>
> e.preventDefault()

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222145158.png)

## 9.7页面加载事件

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222149936.png)

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script>
        //等待页面所有资源加载完毕，就回去执行回调函数
        window.addEventListener('load',function (){})
        const btn = document.querySelector('button');
        btn.addEventListener('click',function (){
            alert(11)
        })
    </script>
</head>
<body>
</body>
</html>
```

## 9.8滚动事件

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222154352.png)

```js
<script>
    window.addEventListener('scroll',function (){
        console.log('滚')
    })
</script>
```

## 9.9页面尺寸事件

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222157564.png)

# 10.0日期对象

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222201892.png)

```js
  // 1. 实例化
  const date = new Date(); // 系统默认时间
  //const date = new Date('2020-05-01') // 指定时间
  // date 变量即所谓的时间对象
  console.log(typeof date)

  // 通过方法分别获取年、月、日，时、分、秒
  const year = date.getFullYear(); // 四位年份
  const month = date.getMonth(); // 0 ~ 11

  const dateTime = date.toLocalString() //2023/12/22 22:06
  const date = date.toLocalDateString() //2023/12/22
  const time = date.toLocalTimeString() //22:08:10
```

```js
    // 1. 实例化
  const date = new Date()
  // 2. 获取时间戳
  console.log(date.getTime())
  // 还有一种获取时间戳的方法
  console.log(+new Date())
  // 还有一种获取时间戳的方法
  console.log(Date.now())
```

## 10.1DOM节点

> DOM树上每一个内容都称之为节点

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222215380.png)

## 10.2查找节点

> 父节点:parentNode
>
> 子节点
>
> 兄弟节点

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222219836.png)

### 10.2.1父节点查找

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222254911.png)

```js
<div class="grandpa">
    <div class="dad">
        <div class="baby">x</div>
    </div>
</div>
<script>
    const baby = document.querySelector('.baby');
    console.log(baby)//返回dom对象
    console.log(baby.parentNode)//返回dom对象
    console.log(baby.parentNode.parentNode)//返回dom对象
</script>
```

### 10.2.2子节点查找

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312222259414.png)







```js
<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
</ul>
<script>
    const ul = document.querySelector('ul');
    // console.log(ul.children)//得到为数组，选择的是亲儿子
    const li2 = document.querySelector('ul li:nth-child(2)');
    console.log(li2.previousElementSibling)
    console.log(li2.nextElementSibling)
</script>
```

### 10.2.3兄弟节点查找

> 下一个兄弟节点:nextElementSibling属性
>
> 上一个兄弟节点:previousElementSibling属性

```js
<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
</ul>
<script>
    const li2 = document.querySelector('ul li:nth-child(2)');
    console.log(li2.previousElementSibling)
    console.log(li2.nextElementSibling)
</script>
```

## 10.3删除节点

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312230019168.png)

```js
<ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
</ul>


<script>
    const ul = document.querySelector('ul');
    //删除节点 父元素.removeChild(子元素)
    ul.removeChild(ul.children[0])
</script>
```

# 11.0数组解构

> 简洁语法

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312230046991.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312230048419.png)

```js
<script>
    const arr = [100,60,80]
    //数组解构 赋值
    const [max,min,avg] = arr
    //const [max,min,avg] = [100,60,80] 等价于上面这一种写法
    //等价于
    // const max = arr[0]
    // const min = arr[1]
    // const avg = arr[2]
    console.log(max)
    console.log(min)
    console.log(avg)
</script>
```

## 11.1对象解构

> 简洁语法
>
> 要求属性名和变量名必须一致才可以

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312230054102.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312230056231.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312230101982.png)

```js
<script>
    //对象结构
    const obj = {
        uname: 'pink老师',
        age: 18
    }
    const {uname,age} = obj
    console.log(uname)
    console.log(age)
    //等价于
    //const uname = obj.uname
    //const age = obj.age
</script>

```

# html

# 1.1基本结构

> 1.想要呈现在网页中的内容写在body标签中
>
> 2.head标签中的内容不会出现在网页中
>
> 3.head标签中的title标签可以指定网页的标题

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261209885.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Title</title>
</head>
<body>
  
</body>
</html>
```



## 1.2注释

> 注释的内容会被浏览器所忽略，不会呈现到页面中，但源代码中依然可见
>
> 注释不可以嵌套

```html
<!-- 下面的文字只能滚动一次 -->
 <marquee loop="1">尚硅谷</marquee>//就是《尚硅谷》三个字在页面里滚动一次
 <!-- 下面的文字可以无限滚动 -->
 <marquee>尚硅谷123</marquee>
```

## 1.3HTML字符编码

> 存储时，对数据进行：编码。
>
> 读取时，对数据进行：解码。

## 1.4排版标签

> p 标签很特殊！它里面不能有： h1~h6 、p、 双 div 标签

| 标签名 | 标签含义                                   | 单/双标签 |
| ------ | ------------------------------------------ | --------- |
| h1~h6  | 标题                                       | 双        |
| p      | 段落                                       | 双        |
| div    | 没有任何含义，用于整体布局(生活中的包装袋) | 双        |

## 1.5块级元素与行内元素

> 1.**div**块级元素：**独占一行**，(排版标签都是块级元素)
>
> 2.**span**行内元素：**不独占一行** 
>
> 3.使用原则： 行内元素 中能写 行内元素，但不能写 块级元素。

## 1.6div和span标签

> div和span都没有语义，就是一个盒子，用来装内容的
>
> div标签可以用来布局，到那时现在一行只能放一个**div**大盒子
>
> span标签用来布局，一行可以多个**span**标签小盒子

## 1.7img标签

> 当图片无法展示时候，有些浏览器会呈现alt属性的值
>
> 尽量不同时修改图片的宽和高，可能会造成比例失调

```html
<img src="图像url" />
```

| 属性     | 属性值   | 说明                             |
| -------- | -------- | -------------------------------- |
| `src`    | 图片路径 | 必须属性                         |
| `alt`    | 文本     | 替换文本，当图片不显示时显示文字 |
| `title`  | 文本     | 提示文本。鼠标放到图像上显示文字 |
| `width`  | 像素     | 图像宽度                         |
| `height` | 像素     | 图像高度                         |
| `border` | 像素     | 图像边框粗细                     |

## 1.8路径

> 1.相对路径：以==当前位置==作为参考点，去建立路径
>
> 2.绝对路径：以==根位置==作为参考点，去建立路径
>
> 注意点
>
> 使用本地绝对路径，一旦更换设备，路径处理起来比较麻烦，所以很少使用。 使用网络绝对路径，确实方便，但要注意：若服务器开启了防盗链，会造成图片引入 失败

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261245266.png)

## 2.1超链接

> #空连接

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261251951.png)

```html
<!-- 跳转其他网页 -->
 <a href="https://www.jd.com/" target="_blank">去京东</a>
 <!-- 跳转本地网页 -->
 <a href="./10_HTML排版标签.html" target="_self">去看排版标签</a>

<!-- 浏览器能直接打开的文件 -->
 <a href="./resource/自拍.jpg">看自拍</a>
 <a href="./resource/小电影.mp4">看小电影</a>
 <a href="./resource/小姐姐.gif">看小姐姐</a>
 <a href="./resource/如何一夜暴富.pdf">点我一夜暴富</a>
 <!-- 浏览器不能打开的文件，会自动触发下载 -->
 <a href="./resource/内部资源.zip">内部资源</a>
 <!-- 强制触发下载 -->
 <a href="./resource/小电影.mp4" download="电影片段.mp4">下载电影</a>
```

## 2.2跳转到锚点

> 注意点:
>
> 1.具有  href 属性的 a标签是超链接，具有name属性的a标签是锚点
>
> 2.name 和id都是区分大小写的，且 name 属性的 a标签是锚点。 id 最好别是数字开头。

```html
//第一步：设置锚点
<!-- 第一种方式：a标签配合name属性 -->
 <a name="test1"></a>
 <!-- 第二种方式：其他标签配合id属性 -->
 <h2 id="test2">我是一个位置</h2>
//第二部：跳转锚点
<!-- 跳转到test1锚点-->
 <a href="#test1">去test1锚点</a>
 <!-- 跳到本页面顶部 -->
 <a href="#">回到顶部</a>
 <!-- 跳转到其他页面锚点 -->
 <a href="demo.html#test1">去demo.html页面的test1锚点</a>
 <!-- 刷新本页面 -->
 <a href="">刷新本页面</a>
 <!-- 执行一段js,如果还不知道执行什么，可以留空，javascript:; -->
 <a href="javascript:alert(1);">点我弹窗</a>
```

### 2.2.1唤起其他指定应用

> 通过 a 标签，可以唤起设备应用程序

```html
<!-- 唤起设备拨号 -->
 <a href="tel:10010">电话联系</a>
 <!-- 唤起设备发送邮件 -->
 <a href="mailto:10010@qq.com">邮件联系</a>
 <!-- 唤起设备发送短信 -->
 <a href="sms:10086">短信联系</a>
```

## 3.0有序列表

```html
<h2>要把大象放冰箱总共分几步</h2>
 <ol>
 <li>把冰箱门打开</li>
 <li>把大象放进去</li>
 <li>把冰箱门关上</li>
 </ol>
```

## 3.1无序列表

```html
<h2>我想去的几个城市</h2>
 <ul>
 <li>成都</li>
 <li>上海</li>
 <li>西安</li>
 <li>武汉</li>
 </ul>
```

## 3.2嵌套列表

```html
<h2>我想去的几个城市</h2>
<ul>
  <li>成都</li>
  <li>
    <span>上海</span>
    <ul>
      <li>外滩</li>
      <li>杜莎夫人蜡像馆</li>
      <li>
        <a href="https://www.opg.cn/">东方明珠</a>
      </li>
      <li>迪士尼乐园</li>
    </ul>
    </li>
	<li>西安</li>
    <li>武汉</li>
</ul>
```

## 3.3自定义列表

> 一个dl就是一个自定义列表，一个 dt 就是一个术语名称，一个dd就是术语描述（可以有多 个）。

```html
<h2>如何高效的学习？</h2>
 <dl>
 <dt>做好笔记</dt>
 <dd>笔记是我们以后复习的一个抓手</dd>
 <dd>笔记可以是电子版，也可以是纸质版</dd>
 <dt>多加练习</dt>
 <dd>只有敲出来的代码，才是自己的</dd>
 <dt>别怕出错</dt>
 <dd>错很正常，改正后并记住，就是经验</dd>
 </dl>
```

## 3.4表格

> table ：表格 
>
> caption ：表格标题 
>
> thead ：表格头部
>
> tbody ：表格主体
>
> tfoot ：表格注脚
>
> tr ：每一行th 、td：每一个单元格（备注：表格头部中用 th ，表格主体、表格脚注中用：td

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261353925.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261357230.png)

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261404060.png)

```html
<table border="1">
  <!-- 表格标题 -->
  <caption>学生信息</caption>
  <!-- 表格头部 -->
  <thead>
  <tr>
    <th>姓名</th>
    <th>性别</th>
    <th>年龄</th>
    <th>民族</th>
    <th>政治面貌</th>
  </tr>
  </thead>
  2. 常用属性
  <!-- 表格主体 -->
  <tbody>
  <tr>
    <td>张三</td>
    <td>男</td>
    <td>18</td>
    <td>汉族</td>
    <td>团员</td>
  </tr>
  <tr>
    <td>李四</td>
    <td>女</td>
    <td>20</td>
    <td>满族</td>
    <td>群众</td>
  </tr>
  <tr>
    <td>王五</td>
    <td>男</td>
    <td>20</td>
    <td>回族</td>
    <td>党员</td>
  </tr>
  <tr>
    <td>赵六</td>
    <td>女</td>
    <td>21</td>
    <td>壮族</td>
    <td>团员</td>
  </tr>
  </tbody>
  <!-- 表格脚注 -->
  <tfoot>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>共计：4人</td>
  </tr>
  </tfoot>
</table>
```

## 3.5跨行跨列

> 1.rowspan ：指定要跨的行数。 
>
> 2.colspan ：指定要跨的列数。

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261411910.png)

## 3.6常用标签

| 标签名 | 标签含义 |
| ------ | -------- |
| br     | 换行     |
| hr     | 分隔     |

## 3.7表单

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261414279.png)

```html
<form action="https://www.baidu.com/s" target="_blank" method="get">
  <input type="text" name="wd">
  <button>去百度搜索</button>
</form>
```

### 3.7.1input文本输入框

> name属性：数据的名称。 
>
> value 属性：输入框的默认输入值。 
>
> maxlength属性：输入框最大可输入长度

```html
<input type = "text">
<input type = "password">
```

### 3.7.2单选框

> name 属性：数据的名称，注意：想要单选效果，多个radio的 ==name 属性值要保持一致==。 value 属性：提交的数据值
>
> checked 属性：让该单选按钮默认选中。 

```html
<input type="radio" name="sex" value="female">女
<input type="radio" name="sex" value="male">男
```

### 3.7.3复选框

> 常用属性如下：： name 属性：数据的名称。 
>
> value 属性：提交的数据值。 
>
> checked属性：让该复选框默认选中。

```html
<input type="checkbox" name="hobby" value="smoke">抽烟
<input type="checkbox" name="hobby" value="drink">喝酒
<input type="checkbox" name="hobby" value="perm">烫头
```

### 3.7.4隐藏域

>  name 属性：数据的名称。 
>
>  value 属性：提交的数据值。 
>
>  checked属性：让该复选框默认选中。

```html
<input type="hidden" name="tag" value="100">
```

### 3.7.5提交按钮

> 注意： 
>
> 1. button 标签 type 属性的默认值是 submit。 
> 1. button不要指定name 属性 
> 1. input标签编写的按钮，使用value属性指定按钮文字。

```html
 <input type="submit" value="点我提交表单">
 <button>点我提交表单</button>
```

### 3.7.6 重置按钮

> 注意点： 
>
> 1. button不要指定name 属性 
> 2. input标签编写的按钮，使用value属性指定按钮文字。

```html
 <input type="reset" value="点我重置">
 <button type="reset">点我重置</button>
```

### 3.7.7普通按钮

> 普通按钮的type值为button，若不写type值是submit会引起表单的提交

```html
 <input type="button" value="普通按钮">
 <button type="button">普通按钮</button>  
```

### 3.7.8文本域

> 1. rows 属性：指定默认显示的行数，会影响文本域的高度。 
> 2. cols 属性：指定默认显示的列数，会影响文本域的宽度。 
> 3. 不能编写type属性，其他属性，与普通文本输入框一致。

```html
<textarea name="msg" rows="22" cols="3">我是文本域</textarea>
```

### 3.7.9下拉框

> 1. n ame 属性：指定数据的名称。 
> 2. option 标签设置 value 属性， 如果没有value属性，提交的数据是option中间的文字；如果设置了 value属性，提交的数据时option中间的文字；==如果设置了value属性，提交的数据就是value的值(建议设置value属性)==
> 3. option 标签设置了  selected 属性，表示默认选中。

```html
<select name="from">
 <option value="黑">黑龙江</option>
 <option value="辽">辽宁</option>
 <option value="吉">吉林</option>
 <option value="粤" selected>广东</option>
 </select>
```

### 3.7.10禁用表单控件

> 给表单控件的标签设置  disabled 既可禁用表单控件
>
> input、textarea、button、select、option都可以设置disabled属性

### 总结

![](https://raw.githubusercontent.com/fightingwithmee/javascript/main/img/202312261447528.png)

