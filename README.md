# MyBatis_Study_Notes
关于MyBatis的杂记

---

#### 1.在 MyBatis 这样的框架中，属性名称通常会遵循驼峰命名，而数据库字段名可能会使用下划线分隔，这时可以通过配置来实现自动映射，比如在 MyBatis 中配置 mapUnderscoreToCamelCase=true，可以将数据库的 id_number 自动映射到 Java 类中的 idNumber。
