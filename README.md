# MyBatis_Study_Notes
关于MyBatis的杂记：

MyBatis 是一个持久层框架，主要用于在应用程序中将对象与数据库记录映射起来。它简化了与数据库的交互，减少了编写 SQL 代码的复杂性。MyBatis 的核心功能是将 SQL 语句与 Java 对象之间进行映射，使得开发者可以更加灵活地控制 SQL 查询。

---

#### 1.在 MyBatis 这样的框架中，属性名称通常会遵循驼峰命名，而数据库字段名可能会使用下划线分隔，这时可以通过配置来实现自动映射，比如在 MyBatis 中配置 mapUnderscoreToCamelCase=true，可以将数据库的 id_number 自动映射到 Java 类中的 idNumber。

---

#### 2.在 XML 文件中，使用 <!-- --> 注释语法可以将代码块注释掉。
例如：

```XML
<!--
    <select id="getByIdWithDish" parameterType="long" resultMap="setmealAndDishMap">
        select a.*,
               b.id     sd_id,
               b.setmeal_id,
               b.dish_id,
               b.name   sd_name,
               b.price  sd_price,
               b.copies
        from setmeal a
                left join
             setmeal_dish b
             on
                 a.id = b.setmeal_id
        where a.id = #{id}
    </select>
-->
```

---

#### 3.启用 MyBatis 的驼峰命名转换

可以在 MyBatis 的配置文件中启用驼峰命名映射，这样数据库中的下划线命名格式会自动映射为实体类中的驼峰命名格式。

如果使用的是 application.yml 或 application.properties 配置文件，可以添加以下配置：

application.yml:
```Mybatis
mybatis:
  configuration:
    map-underscore-to-camel-case: true
```

<br>

application.properties:
```Mybatis
mybatis.configuration.map-underscore-to-camel-case=true
```
---

# 4.MyBatis执行流程

![image](https://github.com/user-attachments/assets/49aedf4b-9ad3-432b-95fc-fdee5d8f7ec9)

![image](https://github.com/user-attachments/assets/4ff9427f-e8b1-4388-9e9d-7ffff6ced3d0)

---

# 5.Mybatis延迟加载使用及原理

![image](https://github.com/user-attachments/assets/c79c2a0b-4829-444a-b2be-28faa9068615)

![image](https://github.com/user-attachments/assets/903ed309-69a0-4f1e-b962-adf09fc51e9a)

![image](https://github.com/user-attachments/assets/2a3c4b9f-7245-4ebe-968a-3aeae6902a62)

---

# 6.Mybatis一级、二级缓存

![image](https://github.com/user-attachments/assets/8a7a14b5-8374-46db-abaa-9c7c0173f857)

![image](https://github.com/user-attachments/assets/f7f0a275-934b-4dc0-ab8a-65cd8dfc6a39)

![image](https://github.com/user-attachments/assets/29b0300a-95c6-4f13-bf4d-8aa733e1501e)

![image](https://github.com/user-attachments/assets/abb00041-c1ed-4939-a1de-ce9fe4608cc3)

![image](https://github.com/user-attachments/assets/3f25847a-afc9-41d6-9d88-6239c276df38)
