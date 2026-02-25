---
metaLinks:
  alternates:
    - https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/setup
---

# 设置

第一步: **将ProtectorAPI添加进你的项目**

**最新版本:** ![](https://img.shields.io/maven-central/v/io.github.lijinhong11/protectorapi-api?label=%20)

**Javadoc:** [https://javadoc.io/doc/io.github.lijinhong11/protectorapi-api/latest/index.html](https://javadoc.io/doc/io.github.lijinhong11/protectorapi-api/latest/index.html)

Maven

```xml
<dependency>
  <groupId>io.github.lijinhong11</groupId>
  <artifactId>protectorapi-api</artifactId>
  <version>VERSION</version>
  <scope>provided</scope>
</dependency>
```

Gradle (Groovy DSL):

```gradle
implementation 'io.github.lijinhong11:protectorapi-api:VERSION'
```

Gradle (Kotlin DSL):

```kts
implementation("io.github.lijinhong11:protectorapi-api:VERSION")
```

**将里面的** `VERSION` **改为最新版本**

**注意:** <mark style="color:red;">**无论如何，请不要将其打包进你的插件里！**</mark>

第二步: 放心使用 :)
