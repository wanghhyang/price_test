1-Design
包括解决方案的总体说明。分层结构、各层调用关系


2-Common
包括解决方案中各层可以共用的基础组件，帮助工具类。
其中
AOP     是一个切面代理层，用于各层各模块的日志记录的代理包装
Caching 是一个缓存层，包括redis的中间件封装，本地缓存对象的处理
Common  是一层Helper类的层。各层需要定义的一些共用处理程序可以放到本层
Logger  是一层日志处理总层，定义了一些处理日志记录的帮助类
MQ      是一层消息。封装消息组件以及消息处理的帮助工具类


3-DataAccess
数据访问层，使用JnsFramework数据库中间件完成对数据库的访问。
其中
BLL层  是业务逻辑处理层。主要是对DAL层的调用，以及对Core层的进一步处理，根据需要可以不适用本层。
DAL层  是数据库访问层。主要包括sql语句的执行
JnsBLL
JnsDAL


4-Entity
实体类、数据库和对象映射类
DTO     是一层数据库存储需要实体类
Entity  是一层用户交互使用的实体类
JnsDict
JnsModel

5-Core
本层是业务逻辑处理的唯一单元，所有的业务处理都要放到本层去做
Core层          是处理系统上非查询的业务逻辑
Query层         是处理系统上查询需要的业务逻辑
ServiceProxy层  是外部接口的引用层


6-Service
改层是服务接口的接口定义层
ApiService层  是服务接口定义层
JobService层  是Schedule调用接口层


7-StartUp
系统输出层，用户交互层
JobHost层         是Job服务的启动层
MQConsumerHost层  是消息消费端的宿主启动层
ServiceHost层     是接口服务的启动层
Web层             是价格系统的用户交互层


8-UnitTests
单元测试层
CommonTest层      是基础组件的单元测试层，2-Common层中需要测试的所有编写都要放到本层
CoreTest层        是业务逻辑的单元测试层，5-Core层中需要测试的所有编写都要放到本层
DataAccessTest层  是数据访问的单元测试层，3-DataAccess层中需要测试的所有编写都要放到本层
Service层         是服务的单元测试层，6-Service层中需要测试的编写都要放到本层