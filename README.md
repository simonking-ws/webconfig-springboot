【特别说明】
> 由于之前的`Github`仓库 https://github.com/simonkingws 的账户二次验证的秘钥丢失，无法继续使用，所以重新创建仓库，维护此项目。

# webconfig-springboot 说明

### 开发环境
JDK1.8+，redis，springboot2.x，dubbo3.x

### 解决的问题
`Springboot`项目的出现，帮我们解决了搭建项目的各种依赖配置等问题，使我们能够快速搭建一个web项目并且能够跑起来，极大的简化了项目的搭建。

为了规范项目，很多项目已经要求全局配置一些公用的组件，例如异常捕获、参数校验、统一返回参数等。所以`webconfig`就是为了解决此类问题，封装好通用的参数并提供可插拔的配置，方便我们规范项目。

### webconfig-spring-boot-starter 特性
依赖：
```xml
<!-- https://central.sonatype.com/artifact/io.github.simonkingws/webconfig-spring-boot-starter -->
<dependency>
    <groupId>io.github.simonkingws</groupId>
    <artifactId>webconfig-spring-boot-starter</artifactId>
    <version>${latest.version}</version>
</dependency>
```
* 统一接口返回。可配置自定义所需要的统一返回实体。
* 统一异常捕获。所有的异常统一处理，也可以自定义异常。并针对需要异常发送通知。
* 统一日期参数的处理。form表单类的日期统一处理，包括Date、LocalDateTime。
* 全局参数RequestHolder.get()。
* 常用过滤器。xss攻击Filter、请求参数去除空格Filter等。
* 常用拦截器。全局参数拦截器。
* 常用注解。重复请求拦截注解。
* 全链路追踪。
* 增加服务内部的链路追踪的注解。
* 增加链路追踪的UI界面。
* 增加重复提交的校验注解。
* 在线运维arthas。

### webconfig-dubbo3 特性
依赖：
```xml
<!-- https://central.sonatype.com/artifact/io.github.simonkingws/webconfig-dubbo3 -->
<dependency>
    <groupId>io.github.simonkingws</groupId>
    <artifactId>webconfig-dubbo3</artifactId>
    <version>${latest.version}</version>
</dependency>
```
* duubo3下全局参数

### webconfig-feign 特性
依赖：
```xml
<!-- https://central.sonatype.com/artifact/io.github.simonkingws/webconfig-feign -->
<dependency>
    <groupId>io.github.simonkingws</groupId>
    <artifactId>webconfig-feign</artifactId>
    <version>${latest.version}</version>
</dependency>
```
* feign调用下的全局参数
* Date参数传递时差问题统一处理

### webconfig-demo 特性
* 应用实例以及case

### webconfig-trace-admin 特性
* 链路追踪的服务，提供webui

**服务调用方法的统计**

![](/images/服务调用的统计.png)

**服务调用的拓扑图**
![](/images/调用拓补图.png)

**服务调用的链路统计**
![](/images/调用链路统计.png)

**服务调用的链路详情**
![](/images/链路详情.png)

**服务调用Top-k**
![](/images/方法调用的top-k.png)

### 使用说明以以及更新日志
详见：https://github.com/simonkingws/webconfig-springboot/blob/main/doc/QuickStart.md
