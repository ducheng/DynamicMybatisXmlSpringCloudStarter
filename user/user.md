# 1，maven 官方仓库查找

## 1.1 复制maven 的坐标 

```
<dependency>
	<groupId>com.github.ducheng</groupId>
	<artifactId>dynamic-mybatis-xml-spring-cloud-starter</artifactId>
	<version>0.0.2</version>
</dependency>
```

# 1.2 在springboot 的resource的目录

bootstrap.yaml 的文件

```yaml
spring:
  cloud:
    mybatis:
      xml:
        dataId : xxxxxxxx //你的nacos 关于日志脱敏的文件dataId
        xmlName: xxxxx   //你要更新的xml文件名称
    nacos:
      discovery:
        server-addr: localhost:8848
      config:
        server-addr: localhost:8848
        namespace: 80d2b616-2c31-409a-855c-1a6b02ee11a6
        file-extension: yaml
        refresh-enabled: true
        extensionConfigs[0]:
          dataId: xxxxxxxx
          refresh: true
```

下面就是愉快的使用了。详细教程和原理请参考 [juejin](https://juejin.cn/post/7217012056113938491?share_token=ff9015b9-e3de-4f31-ad08-af6e8859870d)

