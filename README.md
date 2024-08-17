# MyBatis_Study_Notes
关于MyBatis的杂记：

MyBatis 是一个持久层框架，主要用于在应用程序中将对象与数据库记录映射起来。它简化了与数据库的交互，减少了编写 SQL 代码的复杂性。MyBatis 的核心功能是将 SQL 语句与 Java 对象之间进行映射，使得开发者可以更加灵活地控制 SQL 查询。

---

#### 1.在 MyBatis 这样的框架中，属性名称通常会遵循驼峰命名，而数据库字段名可能会使用下划线分隔，这时可以通过配置来实现自动映射，比如在 MyBatis 中配置 mapUnderscoreToCamelCase=true，可以将数据库的 id_number 自动映射到 Java 类中的 idNumber。
