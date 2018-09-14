treeProfiler
============

监控应用程序，埋点，打印树状结构



把这几个文件放到你的项目中

1、先注入ProfilerApsect

```java
@Configuration
public class DomainConfig {

    @Bean
    public ProfilerApsect profilerApsect(){
        return new ProfilerApsect();
    }
}
```

2、在你需要的类或者方法上添加@ProfilerAnno注解

3、开启日志

```xml
    <logger name="com.yuantu.common.profiler" additivity="false">
        <appender-ref ref="STDOUT" />
    </logger>
```

