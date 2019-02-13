# GraphQL_note
很久以前就知道GraphQL，但是没有理解。今天又看，试着理解。记录一下。

Facebook 推出的，至少有五六年了。但是感觉一直没流行起来。
今天看github 的时候，发现它的新接口采用的 GraphQL 。所以再次研究一下。

GraphQL 官网
https://graphql.cn/

Github 为什么开放了一套 GraphQL 版本的 API？

https://www.oschina.net/news/78302/why-github-open-graphql-api

go   实现 graphQL
https://github.com/CNBlackJ/golesson
golesson(go + gin + graphql )


https://zhuanlan.zhihu.com/p/43615163

从头用go写一个GraphQL服务（1）

https://zhuanlan.zhihu.com/p/34219480

思考： 这样把主动性交给了前端，需要什么数据，后端返回什么数据。  
      好处： 1、这样 省流量。
            2、灵活            
      问题： 后端实现，权限检测。（权限感觉是难点）       

restful 还没怎么明白，这个GraphQL又开始流行起来了。（IT狗，注定要累死呀）

我忽然想到 可以做service层。提供数据   GraphQL  可以做  service层

感觉像是 直接写sql语句的感觉。

忽然想到，猜测实现思路，
    1、权限检测 ===》根据 前端的字段生成sql  ===》 mysql ===>返回前端 
    2、权限检测 ===》后端从mysql 获取一个 object。 根据 前端字段 从 object 上取得 获取需要的字段数据 ===》 返回前端
    
GraphQL 官网
https://graphql.cn/
    
官网有  服务端有go、php 的实现例子 （还有很多其他的语言）
    https://graphql.cn/code/#server-libraries
    
    go https://graphql.cn/code/#go
    php https://graphql.cn/code/#php   https://github.com/webonyx/graphql-php
    
  https://github.com/webonyx/graphql-php  研究这个项目
 https://github.com/webonyx/graphql-php/tree/master/examples/00-hello-world
 
 1、git clone  	https://github.com/webonyx/graphql-php.git
 2、cd graphql-php
 3、composer install
 4、运行 examples  
 按照 graphql-php/examples/  每个例子里面 .md 文件提示。操作、运行例子
 5、选择 00-hello-world 例子
 cd examples/00-hello-world
 6、php -S localhost:8080 ./graphql.php
 7、在打开一个命令行窗口
 curl http://localhost:8080 -d '{"query": "mutation { sum(x: 2, y: 2) }" }'
 8、结果：
 {"data":{"sum":4}}
 9、OK
 
 
 
    
    
