## 数据库配置

```yaml
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    username: ***
    password: ***
    url: jdbc:mysql://39.105.14.128:3306/blog?characterEncoding=utf-8&useSSL=false
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

## 依赖

## 建表

​	  	Type

User - Blog-  Tag

​		comment

comment : 自关联

blog: 标题 内容  首图 标记 浏览次数 赞赏  版权  评论  发布  创建时间 更新时间

tag: 名称

comment: 昵称 邮箱 邮箱 内容 创建时间

user: 昵称 用户名 密码 邮箱 类型 头像 创建时间 更新时间

## 分层

请求处理web---罗逻辑Service -- 持久Dao --数据源

## 约定

**Service/DAO层命名约定：**

- 获取单个对象的方法用get做前缀。
- 获取多个对象的方法用list做前缀。
- 获取统计值的方法用count做前缀。
- 插入的方法用save(推荐)或insert做前缀。
- 删除的方法用remove(推荐)或delete做前缀。
- 修改的方法用update做前缀。