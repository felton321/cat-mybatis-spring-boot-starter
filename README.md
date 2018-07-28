# cat-mybatis-spring-boot-starter

#### 简介
---
大众点评的cat是一款强大的监控工具，在spring boot时代，因为自动配置的出现，使用此starter添加cat对mybatis的监控相当容易，只需添加一个dependency即可，监控核心逻辑基于大众点评的代码，略有修改。

#### 版本
---
1. spring-boot: 1.5.14.RELEASE
2. cat-client: 2.0.0 (后续会开源对cat-client的spring-boot改造，使其不再依赖/data目录)
3. druid: 1.0.18
4. dbcp： 1.4 
#### 使用步骤：
---
1. 首先感谢大众点评的开源奉献。
2. 进入cat的源项目：[https://github.com/dianping/cat](https://github.com/dianping/cat) ,
   按照cat官方的教程打包、部署cat，且需要将cat-client模块的deploy到maven仓库中，本项目需要使用。
3. 下载本项目
4. 根目录下运行 `mvn clean deploy`部署到仓库中。
5. 使用时，在需要监控的项目pom.xml中加入如下依赖即可自动监控mybatis sql：
```
<dependency>
    <groupId>com.github</groupId>
    <artifactId>cat-mybatis-starter</artifactId>
    <version>1.0.0</version>
</dependency>
```
6. 支持dbcp与druid两种连接池，且支持druid多数据源.
7. 如有问题请联系: felton321@sina.com

