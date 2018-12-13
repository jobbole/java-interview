### 1. 列举Spring配置中常用的重要注解。
下面是一些重要的注解：

- @Required
- @Autowired
- @Qualifier
- @Resource
- @PostConstruct
- @PreDestroy

### 2. Spring中的Bean是什么？列举Spring Bean的不同作用域。
Bean 是 Spring 应用的骨架。它们由 Spring IoC 容器管理。换句话说，Bean 是一个由 Spring IoC 容器初始化、装配和管理的对象。   
下面是 Spring Bean 的5种作用域：

- Singleton：每个容器只创建一个实例，也是 Spring Bean 的默认配置。由于非线程安全，因此确保使用时不要在 Bean 中共享实例变量，一面出现数据不一致。
- Prototype：每次请求时创建一个新实例。
- Request：与 prototype 相同，区别在于只针对 Web 应用。每次 HTTP 请求时创建一个新实例。
- Session：每次收到 HTTP 会话请求时由容器创建一个新实例。
- 全局 Session：为每个门户应用（Portlet App）创建一个全局 Session Bean。
