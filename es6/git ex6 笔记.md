-0--基本的命令行操作
clear 向下换行至空
mkdir 创建文件夹 mkdir a a是文件夹的名字
touch 创建文件（文件有后缀名，文件夹没有后缀名）创建多个，touch aaa.txt bbb.css 指定路径创建：touch 1709/aaa.css
rm xx.css删除（直接删除不经过回收站）指定路径：rm 1709/aaa.css 删除文件夹：rm -r 文件夹名 -f强制删除 -rf简写
rm ./*删除当前目录下（./代表当前目录，*是所有）
pwd 查看当前所处位置

git clone git@github.com:Sunny-zz/1709.git

https://github.com/Sunny-zz/1709.git

github 分支   gh-pages         xxx.github.io/app1



master  主分支
index.html style.css公共
about.html   help.html
ls -a  查看隐藏文件   .git 说明本地文件夹是一个github仓库
git branch  --查看当前仓库的分支  *说明  当前位于某个分支   -r 查看远端的分支
git brandch  分支名    --创建新的分支     git branch gh-pages
            当创建新的分支的时候分支里面的内容默认和master分支一样
git checkout 分支名   --切换分支

git checkout -b [yourbranch]  创建新的分支并切换过去



如果一个仓库(除了 xxx.github.io 之外)内有 gh-pages 分支
可使用 用户名.github.io/仓库名  访问 gh-pages 分支下的页面


新建一个仓库  hello    输入网址  xxx.github.io/hello  看到index.html

1.创建仓库 hello  添加了readme.md
2.克隆到本地 git clone
3.新建分支 gh-pages 并切换  git
4.分支上新建 index.html  并上传    git add .   git commit -m'11'   git push
5.访问  git用户名.github.io/hello



github 代码托管工具
本地  网上
1.网上有仓库并且仓库内有内容  仓库克隆到本地   git clone 地址(http ssh)
git add .     git commit -m'xx'     git push      git  pull
2.把本地的项目上传到网上的空仓库
git init     git add .     git commit -m'xx'     git push

ssh-keygen   主目录下会生成 .ssh 文件 内部会生成 两个文件 其中一个就是公钥  id_rsa.pub


分支


1.git用户名.github.io 这个仓库 下的 index.html 能直接访问
用户名.github.io
2.如果一个仓库(除了 xxx.github.io 之外)内有 gh-pages 分支下的 index.html能直接访问
用户名.github.io/仓库名

node   npm
apm install emmet atom编辑器安装插件    atom package manger
nvm  node  version  manger   使用nvm可以安装任何版本的node
nvm ls-remote  查看nvm可以安装那些node版本
nvm use stable
npm 是node的包管理工具  node  packge  manger
新建一个文件夹npm-demo
npm init
npm i jquery --save  安装jquery
npm unninstall jquery  卸载jquery
npm i xx --save-dev 安装工具包
压缩js html css   新的js语法自动编译为es5语法

 .gitignore 文件  git上传时 写在该文件被忽略上传


将本bei地仓库删除   克隆网上的仓库到本地  将node_modules删除
再上传 此时网上就没有了 node_modules
然后本地 npm i  node_modules 就会出现
此时 新建  .gitignore
再上传  此时本地的node_modules 就会上传不上去了
require（“./index.js”）导入index.js导出的变量
路径./指的是当前目录   当导入文件模块的时候路径必须添上 ./
module.exports  导出模块

let ex6 声明变量的方式
const 是用来声明常量的，不允许被修改
1.拥有块级作用域 只要在大括号内声明就会形成作用域
2.同一个作用域下不允许重复声明相同变量
3.变量声明不提升？
4.在let作用域内声明之前使用变量 会报错

解构赋值
//let[a,b,c]=[1,2,3]

//let obj = {name:"hahaha",age:11}
let {name,age} = obj


字符串模板
带变量的字符串用反引号
//var username="hahaha"
var age=20
var c=`my name is ${username},my age is ${age}`
console.log(c)


箭头函数
(1)函数体内的this对象，就是定义时所在的对象，而不是使用时所在的对象。
(2)不可以当做构造函数，也就是说，不可以使用new命令，否则会抛出一个错误
(3)不可以使用arguments对象，该对象在函数体内不存在,如果要用，可以用rest参数替代。
//let [a,b]=[1,2]
箭头左面：参数除了一个以外，必须使用小括号  ，当只有一个参数的时候可以省略小括号
let add = (a,b) => console.log(a+b)
let add = () => c = 1+2

箭头右面：要做的事 当要做的事不止一句的时候必须加上大括号，
        当只有一句执行的时候可以省略大括号，但是同时这句话会被当做该函数的返回值,
        当需要写返回值的时候需要在大括号最后面添加return
add(a,b)

//setTimeout(()=>{},1000)

ex6 函数参数
参数的默认值：函数声明的时候在小括号内部直接给参数赋值相当于给了参数默认值

ex6 函数参数的集合

//let sum = (...rest) => console.log(rest)
sum(1,2,3,4,5,6,7)

扩展操作符 ...
//var arr1=[1,2,3]
var arr2=[4,5,6]
var arr3=[7,8,9]
var newArr = [...arr1,...arr2,...arr3] //拼接数组
console.log(newArr)

//var obj1={
name:"hahaha",
age:20
}
var obj2={
say:function(){
console.log(this.name)
 }
}
var newObj={...obj1,...obj2}
console.log(newObj)

怎么拷贝新数组
//let arr = [1,2,3]
let arr1 = [...arr,4]
console.log(arr.arr1)

//let obj ={name:"hahaha",age:10}
let obj1={...obj}

//let name="hahaha"
let age= 11
let obj={
  name,
  age,
  say(){
    console.log(this.name)
  }
}
obj.say()

class  类
ex6 类的写法
class person{
  constructor(name){
    this.name = name
  }
  say(){
    console.log("hello")
  }
}
//class 内部只能写方法，并且方法之间不能加 逗号
constructor函数 当执行 new+class名时就会默认执行
let people=new person("hahaha")
console.log(people)
people.say()
class Son extends person{
constructor(name,firstName){
//super()处理this指向的  如果继承的话  子类constructor内部必须添加 super()  向super内部传参相当于向继承的父类传参
  super(firstName)
  this.name=name
}
  jump(){
    console.log("jump")
  }
}
let son = new Son("hahaha","张")
son.say()
son.jump()
console.log()
console.log()

use strict 严格模式
consloe.log(new Error("出错了"))

数组的一些方法
过滤
let objArr[
{name:"z",age:10},
{name:"w",age:13},
{name:"l",age:15}
]
filter(function(item,index,array){
return item.age < 15 && item.name==="z"
})
let newArr= objArr.filter(item=>item.age<15 && item.name==="z") 找到age<15并且name==="z"


不修改原对象的情况下，将第一个参数之后的对象合并到第一个对象参数内
object.assign({},obj,{tall:100})

let arr = [1,2,3,4,5]
let num = arr.findIndex(item => item ===3 ) 找到3的索引值
console.log(arr(num)) 2
let newArr = arr.map(item => item * item)
console.log(newArr) 1 4 9 16 25

let arr1=[
{name:"z",age:10},
{name:"w",age:13},
{name:"l",age:15}
]
let obj=arr1.find(item=>item.name==="z")找到"z"

let arr2=[4,2,5,111,3,45,6]排序
arr2.sort((a,b)=>b-a)


Object.keys()

let obj={
  name:"sunny",
  age=20,
  say(){
    console.log(this.name)
  }
}
拿到一个包括obj对象的所有属性值的数组
for(let i in obj){
console.log(obj[i])
}
let arr=Object.keys(obj)拿到一个数组
console.log(arr)

let a = 10
module.exports = a 导入
let b = require("./modules.js")导出
console.log(b)

ex6 模块导入导出
模块导入必须写在当前模块的最顶端
1命名导出 2默认导出
命名导出的话 导入的变量名和导出的必须一致
导入 import
import {a} from './modules'
import * as name from './modules' 当想要把导出内容全部导入的话使用  * as 变量  导入
//import {a as b} from './modules'   a重命名为b    as改名

命名导出
export{a}

默认导出
默认导出只能有一个 不能使用大括号
esport default a



































0
