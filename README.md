# object-Symbol-iterator
为对象部署遍历器接口，并使用es6的for ...of 遍历

#### 知识点：
1.只要有部署了Symbol.iterator遍历器接口，就能遍历
2.Array自带了Symbol.iterator的接口，所以是可遍历的，后来增加 set map的数据结构，同样可以用for ..of遍历
3.obj对象是没有部署遍历接口，所以如果想要遍历的话，必须自己部署
4.for ...of  （例如：for(var value of obj)） 原理：就是在obj对象上部署遍历器接口Symbol.iterator函数，
并且函数只要返回一个iterator对象，iterator对象内部只有next方法，next方法同样是返回一个对象如同{value:xxx,done:false}


#### 问题：
只是把闭包内存中的 index+1
应该如何考虑指针的问题
