# generator-extend
MBG mybatis.generator 扩展 自定义注释 注解 类型转换

#####  plugin元素用来定义一个插件。插件用于扩展或修改通过MyBatis Generator (MBG)代码生成器生成的代码
##### mybatis-generator-core 提供了常用的插件 PluginAdapter 要定制 生成的实体类 接口 及sql 我们只要继承PluginAdapter 并重写相对应的内部方法就好了
##### 简单介绍本文中用到的几个方法 及 参数说明





```
参数
    topLevelClass 对应生成的类
    Interface 对应生成的接口
    Field 对应生成的属性
    Method 对应生成的方法
        参数对象的常用方法
            addAnnotation 增加注解
            addImportedTypes 增加导入的包
            addJavaDocLine 增加注释
            setType 修改属性类型
    introspectedTable 数据库表映射信息
    introspectedColumn 数据库字段映射信息
        
    
PluginAdapter  提供的接口
    modelBaseRecordClassGenerated 修改实体类在此方法
    clientGenerated 修改生成的mapper接口
    modelFieldGenerated 修改生成的属性
    modelSetterMethodGenerated 修改set方法 false不生成
    modelGetterMethodGenerated 修改get方法 false不生成
    clientDeleteByPrimaryKeyMethodGenerated  对应mapper接口方法 DeleteByPrimaryKey方法
    client*****MethodGenerated 对应mapper接口内的各个方法

```
