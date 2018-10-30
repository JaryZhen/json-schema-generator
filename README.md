## 简介
用 Java 语言编写的 Json Schema 生成器
* 将文本格式的 Json 数据转化为 Json Schema；

## Quick Start
* 添加Maven
    
    
    <dependency>
      <groupId>com.github.zhizheng</groupId>
      <artifactId>json-schema-generator</artifactId>
      <version>vipkid-0.0.5</version>
    </dependency>
    
* code


    JsonSchemaConfig jsConfig = new JsonSchemaConfig();
    jsConfig.setPrettyPrint(true);// 优雅打印格式
    jsConfig.setVersion(JsonSchemaVersions.V4.toString());// 默认是 V3
    jsConfig.setPrintRequired(true); // 设置打印 required 属性（开关）
    
    JsonSchemaGenerator jsGenerator = new JsonSchemaGeneratorImpl(jsConfig);
    
    String jsonString = "{\"flag\":\"test\",\"log\":{\"logId\":1,\"logMsg\":\"hello world\"},\"tags\":[\"java\",\"json\",\"schema\",\"generator\"]}";
    String jsonSchemaString = jsGenerator.fromString(jsonString);
    System.out.println(jsonSchemaString);

## 参考资料
https://github.com/temas-hub/jsonSchemaGenerator

https://json-schema.org/understanding-json-schema/index.html
