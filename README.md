# GraphQL_note
很久以前就知道GraphQL，但是没有理解。今天又看，试着理解。记录一下。

Facebook 推出的，至少有五六年了。但是感觉一直没流行起来。
今天看github 的时候，发现它的新接口采用的 GraphQL 。所以再次研究一下。

Github 为什么开放了一套 GraphQL 版本的 API？

https://www.oschina.net/news/78302/why-github-open-graphql-api

go   实现 graphQL
https://github.com/CNBlackJ/golesson

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
