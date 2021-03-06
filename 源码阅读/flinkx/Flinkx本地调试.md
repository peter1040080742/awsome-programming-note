# 编译部署

flinkx版本1.11_release，对应flink版本1.11.3

下载源码后进入jars目录，执行

```
mvn install:install-file -DgroupId=com.dm -DartifactId=Dm7JdbcDriver18 -Dversion=7.6.0.197 -Dpackaging=jar -Dfile=Dm7JdbcDriver18.jar
```

否则编译会提示没kingbase的依赖

执行编译

```
mvn clean install -DskipTests  
```

编译完会多出两个目录

![img](data:image/png;base64,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rSlCff3m0NXrsgyev89SxE08ZkGrVcllQF3VEVkwEY2asNhSXBocIRBsR6dfw3wkzrPx/Jf7I9FmHHVLaDTgC+YvFSYSDhyOMKoKn2Yb2K3llAtrrY/u09P4/E78QfuOdQghqldZr678+z/+yb+Gfqm4gPts4tUl4nEdZssaXu84R1vfYjbFC68rW664bvy91LZTr4/yadbLkSNw9szwtn0DsGHby6kfSafB3TxDZ8czzOY1AsHWTSHqD3rJZODY0dfY7SE+fswH4MavrJtNUY4de8WZvhF0Ovg020Ekml+AMvFikHjUhMOxQHfXE055x3A43hfa+uac5HL5+bBAID/3Fok5AYjFmr4ov+h72rLd529jZQU8nlcM9N8uqY6v9S2EqGzK9d/94bv987509WbRe1fuRil3PLHbUtSa08wv2FhRd3fyvJe2paizJzGblr/av8sVxu/ffhGM3ZqixqQWgmqrWvMKdfY4SxELiaRxX+reicsVJp2s2bTi8zDqEEIcru865Gx19egN+j31saquEl1a3KeKhBBC7Keyn5M7SBJOQghR3cp6Tk4IIYTYCwk5IYQQVUtCTgghRNWSkBNCCFG1JOSEEEJUrf8ClqWE0PSrIswAAAAASUVORK5CYII=)

## 本地开发调试

入口类：com.dtstack.flinkx.test.LocalTest

```
   public static void main(String[] args) throws Exception{
        Properties confProperties = new Properties();
//        confProperties.put("flink.checkpoint.interval", "10000");
//        confProperties.put("flink.checkpoint.stateBackend", "file:///tmp/flinkx_checkpoint");

//        conf.setString("metrics.reporter.promgateway.class","org.apache.flink.metrics.prometheus.PrometheusPushGatewayReporter");
//        conf.setString("metrics.reporter.promgateway.host","127.0.0.1");
//        conf.setString("metrics.reporter.promgateway.port","9091");
//        conf.setString("metrics.reporter.promgateway.jobName","108job");
//        conf.setString("metrics.reporter.promgateway.randomJobNameSuffix","true");
//        conf.setString("metrics.reporter.promgateway.deleteOnShutdown","true");
        System.setProperty("HADOOP_USER_NAME", "hive");

        String jobPath = "/Volumes/Samsung_T5/opensource/flinkx/docs/example/oracle@channel_hive.json";
        JobExecutionResult result = LocalTest.runJob(new File(jobPath), confProperties, null);
        ResultPrintUtil.printResult(result);
        System.exit(0);
    }
```



## 命令行local模式启动

为了方便控制台直接打印日志。修改启动脚本。

![image-20210309102357666](http://image-picgo.test.upcdn.net/img/20210309102357.png)



可以在flinkconf目录下的flink-conf.yml中指定flink的配置

![image-20210309100946763](http://image-picgo.test.upcdn.net/img/20210309100946.png)

这里指定了web-ui的端口。启动后访问8081就可以看到flink ui了。

```
rest.bind-port: 8081
```

启动命令如下：

```
bin/flinkx -mode local -job /Volumes/Samsung_T5/opensource/flinkx/docs/example/LogMiner_stream.json -flinkconf flinkconf
```

![image-20210309101107931](http://image-picgo.test.upcdn.net/img/20210309101107.png)