1.针对一个微服务的断路器监控,但是微服务通常会是多个实例组成的一个集群. 倘若集群里的实例比较多,不可能去挨个监控这些实例,而且有时,根据集群的需要,会动态增加或减少实例, 监控起来更麻烦. <br>
2.所以为了方便监控集群里的多个实例,SpringCloud提供了一个turbine项目,它的作用是把一个集群里的多个实例汇聚在一个turbine里,然后再在断路器监控里查看这个turbine,这样就能够在集群层面进行监控啦. <br>
3.加入依赖:
```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-netflix-turbine</artifactId>
</dependency>
```
4.在application.yml中进行turbine的配置. <br>
5.启动类加入@EnableTurbine注解. <br>