## 概述

之前写过Java，Spring里有一个BeanUtil的东西，可以方便的拷贝两个对象中共有的属性。Go好像没有这种通用的工具类。

用Go写业务的时候，如果属性少还好，如果属性多了会很麻烦，所以就看了看Go的文档，利用放射自己写了一个属性拷贝的方法。

因为主要还是我自己在使用，所以也就不添加LICENSE。

实现起来也很简单的，如果在学习Go，建议自己写一下，以下是我写的博客参考

[Go反射 实现任意类型属性拷贝](https://juejin.im/post/5de48596e51d4532f41b8e8f)


## 使用

#### 下载

```shell script
go get -u github.com/fishyxin/simple-copy-properties
```

#### 导入

```go
import(
    propertyUtil "github.com/fishyxin/simple-copy-properties"
)
```

#### 调用

在需使用的地方调用方法即可

```go
propertyUtil.SimpleCopyProperties(&person, account)
```


**注意，该方法只能用于浅拷贝**