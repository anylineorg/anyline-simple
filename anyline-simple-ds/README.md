这里演示了多数据源的操作以及动态注册数据源  
注意需要在启动类上添加注解  
```
import org.anyboot.jdbc.ds.DynamicDataSourceRegister;
@Import(DynamicDataSourceRegister.class)
```

注意需要在配置文件在配置数据源或动态注册数据源才能切换成功  
动态注册一个数据源
```
import org.anyline.jdbc.ds.DataSourceHolder;
String url = "jdbc:mysql://127.0.0.1:36902/simple_sso?useUnicode=true&characterEncoding=UTF8&useSSL=false&serverTimezone=Asia/Shanghai&allowPublicKeyRetrieval=true";
DataSourceHolder.reg("sso", "com.zaxxer.hikari.HikariDataSource", "com.mysql.cj.jdbc.Driver", url, "root", "root");

```



默认数据源是指配置文件中spring.datasource指定的数据源  



两种方式切换数据源  
1.DataSourceHolder.setDataSource("crm");  
2.查询时在表前 加前缀 <数据源>表  
```
//设置固定数据源，在这之后执行的查询都是查询的crm数据源
DataSourceHolder.setDataSource("crm");
//这里查询的的crm数据源，执行完成后还保持crm数据源
DataSet set = service.querys("crm_customer");


//这里查询erp数据源中的表，执行完成后切换回执行之前的crm数据源，注意并不是默认数据源
set = service.querys("<erp>mm_material");

//这里查询的的crm数据源，而不需要指定<crm>,因为之前已通过DataSourceHolder固定设置了crm数据源
set = service.querys("crm_customer");

```

