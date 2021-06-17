# 变量/类型

## Go快速入门

```go
package main   // 包名

import "fmt"  // 引入的fmt包

// go主入口函数 main函数
func main()  {
	fmt.Println("你好!") // 打印输出
}
```

上面案例是一个基本的入门案例，案例中包含了以下几项
+ **包名** 每个 **.go** 文件都有一个包名，每个go项目只有一个main包名，作为主入口包
+ **引入的fmt包** fmt是Go内置的一个输出和获取的包,fmt就是 这个包的包名
+ **main函数**  main 函数作为主入口函数，也是 每个Go项目只有一个main函数，作为主入口函数
+ **fmt.Println()** fmt包提供的换行输出数据的函数

以上得出 想运行go文件 ,go文件中 必须有 main包名，main函数 go程序才能跑起来

## 变量
#### 变量的介绍
变量，其实相当于内存中开辟一个空间，可以把这个空间就当做变量，把变量在给个名字，我们就可以通过名字 找到对应内存空间中的值
#### 变量的快速入门
```go
package main   // 包名

import "fmt"  // 引入的fmt包

// go主入口函数 main函数
func main()  {
	var i int = 10 // 定义变量切赋值
	fmt.Println("你好!",i) // 使用变量   打印出 ： 你好! 1
}
```
#### 变量的声明方式
```go
package main   // 包名

import "fmt"  // 引入的fmt包

// go主入口函数 main函数
func main()  {
	//1. 声明变量 赋值
	var i int = 10
	// 类型推到
	var name = "张三"
	// 声明并赋值，并且系统自动推断类型，
	age := 19
    // 定义多个变量
    sex,red = 10,"999"
	fmt.Println("你好!",i,name,age,sex,red) // 你好! 10 张三 19 10 999
}
```

::: warning 总结：通过上面的案例得出有点注意事项
+ GO中定义变量必须是有类型的
+ Go在函数中定义 是不能重复名称的,**存在函数作用域**
+ 在main函数外定义的变量为全局变量，也就是整个 **.go文件** 都可以使用这个变量
+ Go中定义的变量类型 为 int类型 不能赋值一个 string字符串类型
+ 定义的变量必须使用,不使用go编译报错
:::

## 常量
#### 常量的介绍
常量和变量类似，区别在于常量定义后就不可修改

#### 常量的快速入门
```go
package main

import "fmt"

func main()  {
	const name string = "张三"
	const age int = 19
	fmt.Println(name,age) // 
}
```
#### 常量的声明方式
```go
package main

import "fmt"

func main()  {
	// 声明赋值
	const name string = "张三"
	// 类型推到
	const age  = 19
	// 定义多变量
	const sex,red = 12,"李四"
	// 一次性定义
	const (
		sex1 = 10
		sex2 = "王五"
		sex3 = true
	)
	fmt.Println(name,age,sex,red) //
}
```

::: warning 总结：通过上面的案例得出有点注意事项
+ GO中定义的常量 和 变量类似 注意事项参考 定义变量的
+ Go中定义的常量 是不可修改的

:::

## 数据类型

在golang中数据类型分
+ 值类型：int,float,bool,string,数组,结构体
+ 引用类型：指针,slice切片,map,管道chan,接口interface,函数

这里只讲 值类型的部分 其他类型放到后面单独做模块讲解

### 整数类型

### 小数类型/浮点型

### 字符串类型

### 布尔型

### 字符串类型


