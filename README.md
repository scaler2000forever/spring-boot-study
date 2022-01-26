spring-boot-study

# 介绍

跟着黑马程序员spring boot教程学习笔记

视频地址：[https://www.bilibili.com/video/BV15b4y1a7yG](https://www.bilibili.com/video/BV15b4y1a7yG)

# 每个子项目对应的视频链接以及一些重要内容的笔记

## 一、基础篇

### 1.入门案例

#### springboot_01_01_quickstart

[P3 基础篇-03-SpringBoot入门案例（Idea联网版）18:12](https://www.bilibili.com/video/BV15b4y1a7yG?p=3)

#### springboot_01_02_quickstart

[P4 基础篇-04-SpringBoot入门案例（官网创建版）06:21](https://www.bilibili.com/video/BV15b4y1a7yG?p=4)

#### springboot_01_03_quickstart

[P5 基础篇-05-SpringBoot入门案例（阿里云版）06:01](https://www.bilibili.com/video/BV15b4y1a7yG?p=5)

#### springboot_01_04_quickstart

[P6 基础篇-06-SpringBoot入门案例（手工制作版）08:34](https://www.bilibili.com/video/BV15b4y1a7yG?p=6)

[P7 基础篇-07-教你一招：隐藏文件或文件夹](https://www.bilibili.com/video/BV15b4y1a7yG?p=7)

[P8 基础篇-08-入门案例解析：parent](https://www.bilibili.com/video/BV15b4y1a7yG?p=8)

[P9 基础篇-09-入门案例解析：starter](https://www.bilibili.com/video/BV15b4y1a7yG?p=9)

[P10 基础篇-10-入门案例解析：引导类](https://www.bilibili.com/video/BV15b4y1a7yG?p=10)

[P11 基础篇-11-入门案例：辅助功能](https://www.bilibili.com/video/BV15b4y1a7yG?p=11)：更换SpringBoot内嵌的默认的web容器从tomcat换成jetty

### 1.1 补充

#### springboot_01_05_rest

[P12 知识加油站-01-REST风格简介](https://www.bilibili.com/video/BV15b4y1a7yG?p=12)

[P13 知识加油站-02-RESTful入门案例](https://www.bilibili.com/video/BV15b4y1a7yG?p=13)

[P14 知识加油站-03-RESTful快速开发](https://www.bilibili.com/video/BV15b4y1a7yG?p=14)

#### springboot_0x_02x_xxxxxxxx
### 2. 基础配置

[P15 基础篇-12-教你一招：复制模块](https://www.bilibili.com/video/BV15b4y1a7yG?p=15)

#### springboot_02_base_configuration

[P16 基础篇-13-属性配置方式](https://www.bilibili.com/video/BV15b4y1a7yG?p=16)

[P17 基础篇-14-基础配置](https://www.bilibili.com/video/BV15b4y1a7yG?p=17)

[P18 基础篇-15-3种配置文件类型](https://www.bilibili.com/video/BV15b4y1a7yG?p=18)

1. properties

2. yml(主流格式)

3. yaml

[P19 基础篇-16-配置文件加载优先级](https://www.bilibili.com/video/BV15b4y1a7yG?p=19)

三种格式共存，优先级从先到后为properties、yml、yaml

[P20 基础篇-17-教你一招：属性提示消失解决方案](https://www.bilibili.com/video/BV15b4y1a7yG?p=20)
### 3. yaml配置文件
#### springboot_03_yaml

[P21 基础篇-18-yaml数据格式](https://www.bilibili.com/video/BV15b4y1a7yG?p=21)

[P22 基础篇-19-读取yaml单一属性数据](https://www.bilibili.com/video/BV15b4y1a7yG?p=22)

[P23 基础篇-20-yaml文件中的变量引用](https://www.bilibili.com/video/BV15b4y1a7yG?p=23)

[P24 基础篇-21-读取yaml全部属性数据](https://www.bilibili.com/video/BV15b4y1a7yG?p=24)

[P25 基础篇-22-读取yaml引用类型属性数据](https://www.bilibili.com/video/BV15b4y1a7yG?p=25)

### 4. 整合Junit
#### springboot_04_junit

[P27基础篇-24-整合JUnit——classes属性](https://www.bilibili.com/video/BV15b4y1a7yG?p=27)

### 5. 整合mybatis
#### springboot_05_mybatis

[P28基础篇-25-SpringBoot整合MyBatis](https://www.bilibili.com/video/BV15b4y1a7yG?p=28)

课程中使用到的数据库脚本

```sql
/*
 Navicat MySQL Data Transfer

 Source Server         : localhost
 Source Server Type    : MySQL
 Source Server Version : 80023
 Source Host           : localhost:3306
 Source Schema         : springboot_db

 Target Server Type    : MySQL
 Target Server Version : 80023
 File Encoding         : 65001

 Date: 20/01/2022 11:50:34
*/

SET NAMES utf8mb4;
SET FOREIGN_KEY_CHECKS = 0;

-- ----------------------------
-- Table structure for tbl_book
-- ----------------------------
DROP TABLE IF EXISTS `tbl_book`;
CREATE TABLE `tbl_book`  (
  `id` int NOT NULL AUTO_INCREMENT,
  `name` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci NULL DEFAULT NULL,
  `type` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci NULL DEFAULT NULL,
  `description` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci NULL DEFAULT NULL,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8mb4 COLLATE = utf8mb4_0900_ai_ci ROW_FORMAT = Dynamic;

-- ----------------------------
-- Records of tbl_book
-- ----------------------------
INSERT INTO `tbl_book` VALUES (1, '三体', '科幻', '大刘的巅峰之作，将中国科幻推向世界舞台。总共分为三部曲：《地球往事》、《黑暗森林》、《死神永生》。');
INSERT INTO `tbl_book` VALUES (2, '格林童话', '童话', '睡前故事。');
INSERT INTO `tbl_book` VALUES (3, 'Spring 5设计模式', '计算机理论', '深入Spring源码剖析Spring源码中蕴含的10大设计模式');
INSERT INTO `tbl_book` VALUES (4, 'Spring MVC+ MyBatis开发从入门到项目实战', '计算机理论', '全方位解析面向Web应用的轻量级框架,带你成为Spring MVC开发高手');
INSERT INTO `tbl_book` VALUES (5, '轻量级Java Web企业应用实战', '计算机理论', '源码级剖析Spring框架,适合已掌握Java基础的读者');
INSERT INTO `tbl_book` VALUES (6, 'Java核心技术卷|基础知识(原书第11版)', '计算机理论', 'Core Java第11版，Jolt大奖获奖作品，针对Java SE9、10、 11全面更新');
INSERT INTO `tbl_book` VALUES (7, '深入理解Java虚拟机', '计算机理论', '5个维度全面剖析JVM,面试知识点全覆盖');
INSERT INTO `tbl_book` VALUES (8, 'Java编程思想(第4版)', '计算机理论', 'Java学习必读经典殿堂级著作!赢得了全球程序员的广泛赞誉');
INSERT INTO `tbl_book` VALUES (9, '零基础学Java (全彩版)', '计算机理论', '零基础自学编程的入门]图书，由浅入深，详解Java语言的编程思想和核心技术');
INSERT INTO `tbl_book` VALUES (10, '直播就该这么做:主播高效沟通实战指南', '市场营销', '李子柒、李佳琦、薇娅成长为网红的秘密都在书中');
INSERT INTO `tbl_book` VALUES (11, '直播销讲实战一本通', '市场营销', '和秋叶一起学系列网络营销书籍');
INSERT INTO `tbl_book` VALUES (12, '直播带货:淘宝、天猫直播从新手到高手', '市场营销', '一本教你如何玩转直播的书， 10堂课轻松实现带货月入3W+');
INSERT INTO `tbl_book` VALUES (13, 'Spring实战第5版', '计算机理论', 'Spring入门经典教程,深入理解Spring原理技术内幕');
INSERT INTO `tbl_book` VALUES (14, 'Spring 5核心原理与30个类手写实战', '计算机理论', '十年沉淀之作，写Spring精华思想');

SET FOREIGN_KEY_CHECKS = 1;
```

[P29 基础篇-26-SpringBoot整合MyBatis常见问题处理](https://www.bilibili.com/video/BV15b4y1a7yG?p=29)

### 6. 整合mybatis-plus

#### springboot_06_mybatis_plus

[P30 基础篇-27-SpringBoot整合MyBatisPlus](https://www.bilibili.com/video/BV15b4y1a7yG?p=30)

### 7. 整合druid数据库连接池

#### springboot_07_druid

[P31 基础篇-28-SpringBoot整合Druid](https://www.bilibili.com/video/BV15b4y1a7yG?p=31)

### 8. springboot基础篇综合案例

#### springboot_08_ssmp

[P32 基础篇-29-SSMP整合案例制作分析](https://www.bilibili.com/video/BV15b4y1a7yG?p=32)

[P33 基础篇-30-模块创建](https://www.bilibili.com/video/BV15b4y1a7yG?p=33)

[P34 基础篇-31-实体类快速开发（lombok）](https://www.bilibili.com/video/BV15b4y1a7yG?p=34)

[P35 基础篇-32-数据层标准开发（基础CRUD）](https://www.bilibili.com/video/BV15b4y1a7yG?p=35)

[P36 基础篇-33-开启MP运行日志](https://www.bilibili.com/video/BV15b4y1a7yG?p=36)

[P38 基础篇-35-数据层标准开发（条件查询）](https://www.bilibili.com/video/BV15b4y1a7yG?p=38)

[P39 基础篇-36-业务层标准开发（基础CRUD）](https://www.bilibili.com/video/BV15b4y1a7yG?p=39)

[P40 基础篇-37-业务层快速开发（基于MyBatisPlus构建）](https://www.bilibili.com/video/BV15b4y1a7yG?p=40)

[P41 基础篇-38-表现层标准开发](https://www.bilibili.com/video/BV15b4y1a7yG?p=41)

[P42 基础篇-39-表现层数据一致性处理（R对象）](https://www.bilibili.com/video/BV15b4y1a7yG?p=42)

[P43 基础篇-40-前后端调用（axios发送异步请求）](https://www.bilibili.com/video/BV15b4y1a7yG?p=43)

[P44 基础篇-41-列表功能](https://www.bilibili.com/video/BV15b4y1a7yG?p=44)

[P45 基础篇-42-添加功能](https://www.bilibili.com/video/BV15b4y1a7yG?p=45)

[P46 基础篇-43-删除功能](https://www.bilibili.com/video/BV15b4y1a7yG?p=46)

[P47 基础篇-44修改功能（加载数据）](https://www.bilibili.com/video/BV15b4y1a7yG?p=47)

[P48 基础篇-45-修改功能](https://www.bilibili.com/video/BV15b4y1a7yG?p=48)

[P49 基础篇-46-异常消息处理](https://www.bilibili.com/video/BV15b4y1a7yG?p=49)

[P50 基础篇-47-分页](https://www.bilibili.com/video/BV15b4y1a7yG?p=50)

[P51 基础篇-48-分页功能维护（删除BUG）](https://www.bilibili.com/video/BV15b4y1a7yG?p=51)

[P52 基础篇-49-条件查询](https://www.bilibili.com/video/BV15b4y1a7yG?p=52)

[P53 基础篇-50-基础篇完结](https://www.bilibili.com/video/BV15b4y1a7yG?p=53)

## 二、运维实用篇

[P54 运维实用篇-51-工程打包与运行](https://www.bilibili.com/video/BV15b4y1a7yG?p=54)

[P55 运维实用篇-52-打包插件](https://www.bilibili.com/video/BV15b4y1a7yG?p=55)

[P56 运维实用篇-53-Boot工程快速启动（Linux版）](https://www.bilibili.com/video/BV15b4y1a7yG?p=56)

```shell
# 后台启动springboot项目jar包
nohup java -jar springboot_08_ssmp-0.0.1-SNAPSHOT.jar > server.log 2>&1 &
# 终止程序
# 查看java -jar 命令对应的进程号
ps -ef | grep "java -jar"
# 终止对应进程
kill -9 <pid>
```

[P57 运维实用篇-54-临时属性](https://www.bilibili.com/video/BV15b4y1a7yG?p=57)

[P58 运维实用篇-55-临时属性（开发环境）](https://www.bilibili.com/video/BV15b4y1a7yG?p=58)

[P59 运维实用篇-56-配置文件4级分类](https://www.bilibili.com/video/BV15b4y1a7yG?p=59)

### 9. 使用自定义配置

#### springboot_09_config

[P60 运维实用篇-57-自定义配置文件](https://www.bilibili.com/video/BV15b4y1a7yG?p=60)

* 方法1：设置程序参数，指定文件名（不包含后缀），如：`--spring.config.name=ebank`

![image-20220121134942535](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220121134942535.png)

* 方法2：指定配置文件的路径，如：`--spring.config.location=classpath:/ebank.yml`

![image-20220121135527619](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220121135527619.png)

* 还可以指定多个配置文件，如：`--spring.config.location=classpath:/ebank.yml,classpath:/ebank-server.yml`

![image-20220121140035574](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220121140035574.png)

### 10. 多环境配置

#### springboot_10_profiles

[P61 运维实用篇-58-多环境开发（yaml版）](https://www.bilibili.com/video/BV15b4y1a7yG?p=61)

单文件版：

application.yml文件：

```yaml
# 应用环境
# 公共配置
spring:
  profiles:
    active: dev
---
# 生产环境
spring:
  config:
    activate:
      on-profile: pro
server:
  port: 80
---
spring:
  config:
    activate:
      on-profile: dev
server:
  port: 8080
---
# 测试环境
spring:
  config:
    activate:
      on-profile: test
server:
  port: 8888
```

[P62 运维实用篇-59-多环境开发多文件版（yaml版）](https://www.bilibili.com/video/BV15b4y1a7yG?p=62)

##### yaml多文件版

application.yml

```yaml
# 应用环境
# 公共配置
spring:
  profiles:
    active: test
```

application-dev.yml

```yaml
# 开发环境
server:
  port: 8080
```

application-pro.yml

```yaml
# 生产环境
server:
  port: 80
```

application-test.yml

```yaml
# 测试环境
server:
  port: 8888
```

[P63 运维实用篇-60-多环境开发多文件版（properties版）](https://www.bilibili.com/video/BV15b4y1a7yG?p=63)

##### properties多文件版

application.properties

```properties
# 应用环境
spring.profiles.active=test
```

application-dev.properties

```properties
# 开发环境
server.port=80
```

application-pro.properties

```properties
# 生产环境
server.port=8080
```

application-test.properties

```properties
# 测试环境
server.port=8888
```

[P64 运维实用篇-61-多环境分组管理](https://www.bilibili.com/video/BV15b4y1a7yG?p=64)

使用group属性配置同组的配置文件，active可以直接使一组配置文件同时生效

application.yml

```yaml
#spring:
#  profiles:
#    active: dev
#    include: devDB, devMVC

spring:
  profiles:
    active: dev
    group:
      "dev": devDB, devMVC
      "pro": proDB, proMVC
      "test": testDB, TestMVC
```

application-dev.yml

```yaml
server:
  port: 80
```

application-devDB.yml

```yaml
server:
  port: 81
```

application-devMVCyml

```yaml
server:
  servlet:
    context-path: /ebank
  port: 82
```

观察启动日志，配置文件加载的顺序为 : The following profiles are active: dev,devDB,devMVC

[P65 运维实用篇-62-多环境开发控制](https://www.bilibili.com/video/BV15b4y1a7yG?p=65)

maven中使用多环境，然后在springboot中读取maven中的配置

pom.xml中的配置

```xml
<!--设置多环境-->
<profiles>
    <profile>
        <id>env_dev</id>
        <properties>
            <profile.active>dev</profile.active>
        </properties>
        <activation>
            <activeByDefault>true</activeByDefault>
        </activation>
    </profile>
    <profile>
        <id>env_pro</id>
        <properties>
            <profile.active>pro</profile.active>
        </properties>

    </profile>
    <profile>
        <id>env_test</id>
        <properties>
            <profile.active>test</profile.active>
        </properties>
        <activation>
            <activeByDefault>true</activeByDefault>
        </activation>
    </profile>
</profiles>
```

application.yml中的配置

```yaml
#spring:
#  profiles:
#    active: dev
#    include: devDB, devMVC

spring:
  profiles:
    active: @profile.active@
    group:
      "dev": devDB, devMVC
      "pro": proDB, proMVC
      "test": testDB, TestMVC
```

### 11. 记录日志

#### springboot_11_log

[P66 运维实用篇-63-日志基础操作](https://www.bilibili.com/video/BV15b4y1a7yG?p=66)

[P67 运维实用篇-64-教你一招：快速创建日志对象](https://www.bilibili.com/video/BV15b4y1a7yG?p=67)

[P68 运维实用篇-65-日志输出格式控制](https://www.bilibili.com/video/BV15b4y1a7yG?p=68)

[P69 运维实用篇-66-文件记录日志（运维实用篇完结）](https://www.bilibili.com/video/BV15b4y1a7yG?p=69)

## 三、开发实用篇

### 12. 热部署

#### springboot_12_hot_deploy

[P70 开发实用篇-67-手工启动热部署](https://www.bilibili.com/video/BV15b4y1a7yG?p=70)

想要拥有热部署的功能，需要在pom.xml文件中添加如下依赖：

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <optional>true</optional>
</dependency>
```

[P71 开发实用篇-68-自动启动热部署](https://www.bilibili.com/video/BV15b4y1a7yG?p=71)

自动启动热部署，即，`CTRL + F9`编译的操作操作由程序自动完成，需要进行如下配置：

1. 在设置中勾选

![image-20220122192552887](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220122192552887.png)

2. 按快捷键`CTRL + SHIFT + ALT + /`，在弹出的菜单中选择第一项，注册表，或者直接按`CTRL + ALT + M`调出注册表；

![image-20220122193117350](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220122193117350.png)

3. 在注册表项中勾选`compiler.automake.allow.when.app.running`
![image-20220122194309467](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220122194309467.png)
4. idea新版本2021.3.1中在注册表中找不到改选项，需要在高级设置中进行设置。
    ![image-20220122193933991](C:\Users\CandyWall\AppData\Roaming\Typora\typora-user-images\image-20220122193933991.png)

[P72 开发实用篇-69-热部署范围配置](https://www.bilibili.com/video/BV15b4y1a7yG?p=72)

[P73 开发实用篇-70-关闭热部署功能](https://www.bilibili.com/video/BV15b4y1a7yG?p=73)

application.yml

```yaml
spring:
  # 热部署范围配置
  devtools:
    restart:
      # 设置不参与热部署的文件和文件夹（即修改后不重启）
      exclude: static/**,public/**,config/application.yml
      #是否可用
      enabled: false
```

如果配置文件比较多的时候找热部署对应配置比较麻烦，可以在springboot启动类的main方法中设置，此处设置的优先级将比配置文件高，一定会生效。

```java
System.setProperty("spring.devtools.restart.enabled", "false");
```

### 13. 属性绑定

#### springboot_13_configuration

[P74 实用开发篇-71-第三方bean属性绑定](https://www.bilibili.com/video/BV15b4y1a7yG?p=74)

1. 先在要配置的类上面加`@Component`注解将该类交由spring容器管理；

2. `@ConfigurationProperties(prefix="xxx")`，`xxx`跟`application.yml`配置文件中的属性对应；

3. 如果多个配置类想统一管理也可以通过`@EnableConfigurationProperties({xxx.class, yyy.class})`的方式完成配置，不过该注解会与@Component配置发生冲突，二选一即可；

4. 第三方类对象想通过配置进行属性注入，可以通过创建一个方法，在方法体上加@Bean和@ConfigurationProperties(prefix="xxx")注解，然后方法返回这个第三方对象的方式。

5. 使用@ConfigurationProperties(prefix="xxx")注解后idea工具会报一个警告Spring Boot Configuration Annotation Processor not configured

   ![image-20220123172141642](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220123172141642.png)

   只需要在pom.xml中加上如下依赖刷新即可消除该警告

   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-configuration-processor</artifactId>
   </dependency>
   ```

[P75 实用开发篇-72-松散绑定](https://www.bilibili.com/video/BV15b4y1a7yG?p=75)

@ConfigurationProperties绑定属性支持属性名宽松绑定，又叫松散绑定。

比如要将ServerConfig.class作为配置类，并通过配置文件application.yml绑定属性

ServerConfig.class

```java
@Component
@ConfigurationProperties(prefix = "serverconfig")
@Data
public class ServerConfig {
    private String ipAddress;
    private int port;
    private long timeout;
}
```

application.yml

```yaml
serverConfig:
  # ipAddress: 192.168.0.1 # 驼峰模式
  # ipaddress: 192.168.0.1
  # IPADDRESS: 192.168.0.1
  ip-address: 192.168.0.1 # 主流配置方式，烤肉串模式
  # ip_address: 192.168.0.1 # 下划线模式
  # IP_ADDRESS: 192.168.0.1 # 常量模式
  # ip_Add_rEss: 192.168.0.1
  # ipaddress: 192.168.0.1
  port: 8888
  timeout: -1
```

以`ipAddress`属性为例，上面的多种配置方式皆可生效，这就是松散绑定。而`@Value`不支持松散绑定，必须一一对应。

`@ConfigurationProperties(prefix="serverconfig")`中的`prefix`的值为`serverconfig`或者`server-config`，如果是`serverConfig`就会报错，这与松散绑定的前缀命名规范有关：仅能使用纯小写字母、数字、中划线作为合法的字符

[P76 实用开发篇-73-常用计量单位应用](https://www.bilibili.com/video/BV15b4y1a7yG?p=76)

 ```java
//@Component
@ConfigurationProperties(prefix = "server-config")
@Data
public class ServerConfig {
    private String ipAddress;
    private int port;
    @DurationUnit(ChronoUnit.MINUTES)
    private Duration timeout;

    @DataSizeUnit(DataUnit.MEGABYTES)
    private DataSize dataSize;
}
 ```

[P77 实用开发篇-74-bean属性校验](https://www.bilibili.com/video/BV15b4y1a7yG?p=77)

引入Bean属性校验框架的步骤：

1. 在pom.xml中添加JSR303规范和hibernate校验框架的依赖：

```xml
<!--导入JSR303规范-->
<dependency>
    <groupId>javax.validation</groupId>
    <artifactId>validation-api</artifactId>
</dependency>
<!--使用hibernate框架提供的校验器-->
<dependency>
    <groupId>org.hibernate.validator</groupId>
    <artifactId>hibernate-validator</artifactId>
</dependency>
```

2. 在要校验的类上加@Validated注解
3. 设置具体的校验规则，如：@Max(value=8888, message="最大值不能超过8888")

```java
@ConfigurationProperties(prefix = "server-config")
@Data
// 2.开启对当前bean的属性注入校验
@Validated
public class ServerConfig {
    private String ipAddress;
    // 设置具体的规则
    @Max(value = 8888, message = "最大值不能超过8888")
    @Min(value = 1000, message = "最小值不能低于1000")
    private int port;
    @DurationUnit(ChronoUnit.MINUTES)
    private Duration timeout;

    @DataSizeUnit(DataUnit.MEGABYTES)
    private DataSize dataSize;
}
```

[P78 实用开发篇-75-进制数据转换规则](https://www.bilibili.com/video/BV15b4y1a7yG?p=78)

进制转换中的一些问题：

如application.yml文件中对数据库有如下配置：

```yaml
datasource:
  driverClassName: com.mysql.cj.jdbc.Driver123
  # 不加引号读取的时候默认解析为了8进制数，转成十进制就是87
  # 所以想让这里正确识别，需要加上引号
  # password: 0127
  password: "0127"
```

### 14. 测试相关

[P79 实用开发篇-76-加载测试专用属性](https://www.bilibili.com/video/BV15b4y1a7yG?p=79)

#### springboot_14_test

`@SpringBootTest`注解中可以设置`properties`和`args`属性，这里的args属性的作用跟idea工具中自带的程序参数类似，只不过这里的配置是源码级别的，会随着源码的移动而跟随，而idea中的程序参数的配置会丢失。并且这里的args属性的配置的作用范围比较小，仅在当前测试类生效。

application.yml

```yaml
test:
  prop: testValue
```

PropertiesAndArgsTest.java

```java
// properties属性可以为当前测试用例添加临时的属性配置
//@SpringBootTest(properties = {"test.prop=testValue1"})
// args属性可以为当前测试用例添加临时的命令行参数
//@SpringBootTest(args = {"--test.prop=testValue2"})
// 优先级排序： args > properties > 配置文件
@SpringBootTest(args = {"--test.prop=testValue2"}, properties = {"test.prop=testValue1"})
class PropertiesAndArgsTest {
    @Value("${test.prop}")
    private String prop;
    @Test
    public void testProperties() {
        System.out.println("prop = " + prop);
    }
}
```

[P80 实用开发篇-77-加载测试专用配置](https://www.bilibili.com/video/BV15b4y1a7yG?p=80)

某些测试类中需要用到第三方的类，而其他测试类则不需要用到，这里可以在类上加载@Import({xxx.class， yyy.class})

[P81 实用开发篇-78-测试类中启动web环境](https://www.bilibili.com/video/BV15b4y1a7yG?p=81)

[P82 实用开发篇-79-发送虚拟请求](https://www.bilibili.com/video/BV15b4y1a7yG?p=82)

[P83 实用开发篇-80-匹配响应执行状态](https://www.bilibili.com/video/BV15b4y1a7yG?p=83)

[P84 实用开发篇-81-匹配响应体](https://www.bilibili.com/video/BV15b4y1a7yG?p=84)

[P85 实用开发篇-82-匹配响应体（json）](https://www.bilibili.com/video/BV15b4y1a7yG?p=85)

[P86 实用开发篇-83-匹配响应头](https://www.bilibili.com/video/BV15b4y1a7yG?p=86)

表现层BookController.java

```java
@RestController
@RequestMapping("/books")
public class BookController {
    /*@GetMapping("/{id}")
    public String getById(@PathVariable int id) {
        System.out.println("id = " + id);
        return "getById...";
    }*/

    @GetMapping("/{id}")
    public Book getById(@PathVariable int id) {
        System.out.println("id = " + id);
        Book book = new Book();
        book.setId(5);
        book.setName("神秘岛");
        book.setType("科幻");
        book.setDescription("《神秘岛》是法国科幻小说家儒勒·凡尔纳创作的长篇小说，是他写的三部曲之一。");

        return book;
    }
}
```

对应的测试类WebTest.java

```java
@SpringBootTest(webEnvironment = SpringBootTest.WebEnvironment.RANDOM_PORT)
// 开启虚拟mvc调用
@AutoConfigureMockMvc
public class WebTest {
    @Test
    public void testRandomPort() {
    }

    @Test
    public void testWeb(@Autowired MockMvc mvc) throws Exception {
        // 创建虚拟请求，当前访问 /books
        MockHttpServletRequestBuilder builder = MockMvcRequestBuilders.get("/books/5");
        mvc.perform(builder);
    }

    @Test
    public void testStatus(@Autowired MockMvc mvc) throws Exception {
        MockHttpServletRequestBuilder builder = MockMvcRequestBuilders.get("/books1/6");
        ResultActions action = mvc.perform(builder);
        // 设定预期值，与真实值进行比较，成功测试通过，失败测试不通过
        // 定义本次调用的预期值
        StatusResultMatchers srm = MockMvcResultMatchers.status();
        // 预计本次调用成功的状态码：200
        ResultMatcher ok = srm.isOk();
        // 添加预计值到本次调用过程中进行匹配
        action.andExpect(ok);
    }

    @Test
    public void testBody(@Autowired MockMvc mvc) throws Exception {
        MockHttpServletRequestBuilder builder = MockMvcRequestBuilders.get("/books/6");
        ResultActions action = mvc.perform(builder);
        // 设定预期值，与真实值进行比较，成功测试通过，失败测试不通过
        // 定义本次调用的预期值
        ContentResultMatchers crm = MockMvcResultMatchers.content();
        // 预计本次调用成功的状态码：200
        ResultMatcher rm = crm.string("getById...");
        // 添加预计值到本次调用过程中进行匹配
        action.andExpect(rm);
    }

    @Test
    public void testJson(@Autowired MockMvc mvc) throws Exception {
        MockHttpServletRequestBuilder builder = MockMvcRequestBuilders.get("/books/7");
        ResultActions action = mvc.perform(builder);
        // 设定预期值，与真实值进行比较，成功测试通过，失败测试不通过
        // 定义本次调用的预期值
        ContentResultMatchers jsonMatcher = MockMvcResultMatchers.content();
        ResultMatcher rm = jsonMatcher.json("{\"id\":5,\"name\":\"神秘岛\",\"type\":\"科幻\",\"description\":\"《神秘岛》是法国科幻小说家儒勒·凡尔纳创作的长篇小说，是他写的三部曲之一。1\"}");
        action.andExpect(rm);
    }

    @Test
    public void testContentType(@Autowired MockMvc mvc) throws Exception {
        MockHttpServletRequestBuilder builder = MockMvcRequestBuilders.get("/books/7");
        ResultActions action = mvc.perform(builder);
        // 设定预期值，与真实值进行比较，成功测试通过，失败测试不通过
        // 定义本次调用的预期值
        HeaderResultMatchers hrm = MockMvcResultMatchers.header();
        ResultMatcher rm = hrm.string("Content-Type", "application/json");
        action.andExpect(rm);
    }

    @Test
    // 完整测试
    public void testGetById(@Autowired MockMvc mvc) throws Exception {
        MockHttpServletRequestBuilder builder = MockMvcRequestBuilders.get("/books/8");
        ResultActions action = mvc.perform(builder);

        // 1、比较状态码
        StatusResultMatchers statusResultMatchers = MockMvcResultMatchers.status();
        ResultMatcher statusResultMatcher = statusResultMatchers.isOk();
        action.andExpect(statusResultMatcher);

        // 2、比较返回值类型
        HeaderResultMatchers headerResultMatchers = MockMvcResultMatchers.header();
        ResultMatcher headerResultMatcher = headerResultMatchers.string("Content-Type", "application/json");
        action.andExpect(headerResultMatcher);

        /// 3、比较json返回值
        ContentResultMatchers contentResultMatchers = MockMvcResultMatchers.content();
        ResultMatcher jsonResultMatcher = contentResultMatchers.json("{\"id\":5,\"name\":\"神秘岛\",\"type\":\"科幻\",\"description\":\"《神秘岛》是法国科幻小说家儒勒·凡尔纳创作的长篇小说，是他写的三部曲之一。\"}");
        action.andExpect(jsonResultMatcher);
    }
}
```

[P87 实用开发篇-84-业务层测试事务回滚](https://www.bilibili.com/video/BV15b4y1a7yG?p=87)

测试过程中对数据库的增删改操作的影响是否回滚，由下面两个注解控制，需要在测试类上加：

@Transactional，@Rollback(value=true)：回滚，@Rollback(value=true)为默认值，也可以省略；

@Transactional，@Rollback(value=false)：不回滚，跟什么注解都不加的效果一样。

[P88 实用开发篇-85-测试用例设置随机数据](https://www.bilibili.com/video/BV15b4y1a7yG?p=88)

可以把测试用例中的属性值都按照一定规则设置成随机值，可以让测试结果更具有普适性。并且可以把测试用例的属性的随机规则写在配置文件中，方便更改。

application.yml

```yaml
testcase:
  randomBook:
    id: ${random.int}
    id2: ${random.int(10)} # 生成10以内的整数
    type: ${random.int(5, 10)} # 生成5-10之间的整数
    name: 糖果墙${random.value}
    uuid: ${random.uuid}
    publicTime: ${random.long}
```

BookCase.java

```java
@Data
@Component
@ConfigurationProperties(prefix = "test-case.random-book")
public class BookCase {
    private Integer id;
    private Integer id2;
    private String type;
    private String name;
    private String uuid;
    private Long publishTime;
}
```

### 15. 数据层解决方案

#### springboot_15_01_datasource

[P89 实用开发篇-86-内置数据源](https://www.bilibili.com/video/BV15b4y1a7yG?p=89)

在springboot项目中使用Druid数据源，需要先在pom.xml中加上Druid的依赖：

```xml
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid-spring-boot-starter</artifactId>
    <version>1.2.8</version>
</dependency>
```

然后在application.yml中有两种配置方法，两种方法实现的效果一样

```yaml
# 配法1：
spring:
  datasource:
    druid:
      driver-class-name: com.mysql.cj.jdbc.Driver
      url: jdbc:mysql://localhost:3306/springboot_db?serverTimezone=UTC
      username: root
      password: 123

# 配法2：
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/springboot_db?serverTimezone=UTC
    username: root
    password: 123
    type: com.alibaba.druid.pool.DruidDataSource # 去掉type属性，Druid数据源依然会启用
```

配法2去掉type属性后，再启动项目，发现Druid数据源依然启用了，这是由于引入了Druid数据源的依赖后，springboot会自动配置Druid。

如果不引入Druid数据源的依赖，springboot默认的数据源是Hikari数据源

```yaml
# 默认为Hikari数据源
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/springboot_db?serverTimezone=UTC
    username: root
    password: 123
    
# Hikari数据源详细配置，这里需要注意url需要和Hikari属性并列，而Hikari下的jdbc-url无效
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/springboot_db?serverTimezone=UTC
    hikari:
      # jdbc-url: jdbc:mysql://localhost:3306/springboot_db?serverTimezone=UTC # 此项无效
      driver-class-name: com.mysql.cj.jdbc.Driver
      username: root
      password: 123
      maximum-pool-size: 50
      minimum-idle: 30
      idle-timeout: 30000
```

#### springboot_15_02_jdbc_template

[P90 实用开发篇-87-JdbcTemplate](https://www.bilibili.com/video/BV15b4y1a7yG?p=90)

使用JdbcTemplate

1. 在pom.xml中加入相关依赖

2. application.yml中配置数据源，另外还可以对JdbcTemplate进行一些简单的配置

   ```yaml
   # 配置数据库和连接池
   spring:
     datasource:
       url: jdbc:mysql://localhost:3306/springboot_db?serverTimezone=UTC
       hikari:
         driver-class-name: com.mysql.cj.jdbc.Driver
         username: root
         password: TGQ@candywall123
         maximum-pool-size: 50
         minimum-idle: 30
         # idle-timeout: 30000
   
     # JdbcTemplate的一些配置
     jdbc:
       template:
         query-timeout: 30s # 指定查询超时时间
         max-rows: 500 # 最大查询条数
         fetch-size: 500 # 数据条数比较多的时候，一次拿多少条数据
   ```

3. 测试类

   ```java
   @SpringBootTest
   class JdbcTemplateApplicationTests {
       @Autowired
       private JdbcTemplate jdbcTemplate;
       @Test
       void testJdbcTemplateSelect() {
           String sql = "select * from tbl_book";
           // List<Map<String, Object>> maps = jdbcTemplate.queryForList(sql);
           // System.out.println(maps);
           RowMapper<Book> rm = new RowMapper<Book>() {
               @Override
               public Book mapRow(ResultSet rs, int rowNum) throws SQLException {
                   Book book = new Book();
                   book.setId(rs.getInt("id"));
                   book.setName(rs.getString("name"));
                   book.setType(rs.getString("type"));
                   book.setDescription(rs.getString("description"));
                   return book;
               }
           };
           List<Book> bookList = jdbcTemplate.query(sql, rm);
           bookList.forEach(System.out::println);
       }
       
       @Test
       void testJdbcTemplateInsert() {
           String sql = "insert into tbl_book values(null, ?, ?, ?)";
           jdbcTemplate.update(sql, "springboot1", "springboot2", "springboot3");
       }
   }
   ```

#### springboot_15_03_h2

[P91 实用开发篇-88-H2数据库](https://www.bilibili.com/video/BV15b4y1a7yG?p=91)

使用H2数据库

1. 在pom.xml中加入相关依赖

2. 在application.yml中配置数据源并且启用H2数据库的控制台

   ```yaml
   server:
     port: 80
     
   spring:
     # 配置数据库和连接池
     datasource:
       url: jdbc:h2:~/test
       hikari:
         driver-class-name: org.h2.Driver
         username: sa
         password: 123456
   
     # 启用H2的控制台
     h2:
       console:
         enabled: true
         path: /h2
   ```

3. 在浏览器中输入访问H2控制台地址

   ![image-20220124170318554](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220124170318554.png)

4. 输入默认密码：123456，然后点连接，会跳转到控制台主页

   ![image-20220124170509519](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220124170509519.png)

5. 可以写sql语句建表，并插入几条数据

   ```sql
   create table tbl_book(
      id int,
      type varchar,
      name varchar,
      description varchar
   );
   
   insert into tbl_book values(1, 'springboot1', 'springboot2', 'springboot3');
   insert into tbl_book values(2, 'springboot4', 'springboot5', 'springboot6');
   insert into tbl_book values(3, 'springboot7', 'springboot8', 'springboot9');
   insert into tbl_book values(4, 'springboot10', 'springboot11', 'springboot12');
   ```

   

   ![image-20220124170949962](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220124170949962.png)

   ![image-20220124171610075](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220124171610075.png)

   查询tbl_book表中的数据

   ```sql
   select * from tbl_book;
   ```

   ![image-20220124171707774](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220124171707774.png)

6. 写代码连接H2数据库，需要注意启动测试类连接H2数据库的时候需要将之前的H2控制台的springboot程序先停止，否则会造成端口占用，测试类报错。

   测试类：

   ```java
   @SpringBootTest
   class H2ApplicationTests {
       @Autowired
       private JdbcTemplate jdbcTemplate;
   
       @Test
       public void testH2Select() {
           String sql = "select * from tbl_book";
   
           RowMapper<Book> rm = new RowMapper<Book>() {
               @Override
               public Book mapRow(ResultSet rs, int rowNum) throws SQLException {
                   Book book = new Book();
                   book.setId(rs.getInt("id"));
                   book.setName(rs.getString("name"));
                   book.setType(rs.getString("type"));
                   book.setDescription(rs.getString("description"));
                   return book;
               }
           };
           List<Book> bookList = jdbcTemplate.query(sql, rm);
           bookList.forEach(System.out::println);
       }
   
       @Test
       public void testH2Save() {
           String sql = "insert into tbl_book values(?, ? ,? ,?)";
           jdbcTemplate.update(sql, 5, "啊哈算法", "计算机", "数据结构和算法");
       }
   }
   ```

7. H2数据库线上运行时请务必关闭。

    ```apl
    bind 0.0.0.0
    protected-mode no
    port 6379
    timeout 0
    save 900 1 # 900s内至少一次写操作则执行bgsave进行RDB持久化
    save 300 10
    save 60 10000
    rdbcompression yes
    dbfilename dump.rdb
    dir /data
    appendonly yes
    appendfsync everysec
    requirepass 12345678
    ```

#### springboot_15_04_redis

[P92 实用开发篇-89-redis下载安装与基本使用](https://www.bilibili.com/video/BV15b4y1a7yG?p=92)

* windows版下载地址：[https://github.com/tporadowski/redis/releases](https://github.com/tporadowski/redis/releases)

* linux版下载地址：[https://redis.io/](https://redis.io/)

* 在linux上安装redis除了最原始的方法外，推荐使用docker-compose一键启动redis，非常方便

redis.conf
```java
bind 0.0.0.0
protected-mode no
port 6379
timeout 0
save 900 1 # 900s内至少一次写操作则执行bgsave进行RDB持久化
save 300 10
save 60 10000
rdbcompression yes
dbfilename dump.rdb
dir /data
appendonly yes
appendfsync everysec
requirepass 123456
```
docker-compose.yml
```yaml
version: '3'

services:
  redis:
    image: redis:latest
    container_name: redis
    restart: always
    ports:
      - 6379:6379
    volumes:
      - ./redis.conf:/etc/redis/redis.conf:rw
      - ./data:/data:rw
    command: ["redis-server","/etc/redis/redis.conf"]
```

我的redis安装在虚拟机中的linux系统上，可以通过以下两种方式测试连通性：

1. 通过windows版redis自带的`redis-cli`来远程连接linux上的redis服务，指令如下：

```bash
redis-cli.exe -h 192.168.0.110 -p 6379 -a "123456" # 123456是密码
```

2. 还可以使用`AnotherRedisDesktopManager`：这是一款非常稳定并且拥有美观的图形界面的redis客户端，操作起来也是相当简单，一看就会用，下载地址：[https://github.com/qishibo/AnotherRedisDesktopManager/releases](https://github.com/qishibo/AnotherRedisDesktopManager/releases)

[P93 实用开发篇-90-SpringBoot整合Redis](https://www.bilibili.com/video/BV15b4y1a7yG?p=93)

1. 在pom.xml中加入spring整合redis的依赖

    ```xml
    <!--springboot整合redis-->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-redis</artifactId>
    </dependency>
    ```

2. application.yml

    ```yaml
    spring:
      # redis配置
      redis:
        host: 192.168.0.110
        port: 6379
        password: 123456
    ```

3. 测试类

   ```java
   @SpringBootTest
   class RedisApplicationTests {
       @Autowired
       private StringRedisTemplate redisTemplate;
   
       @Test
       public void testSet() {
           ValueOperations valueOperations = redisTemplate.opsForValue();
   
           valueOperations.set("age", "41");
       }
       @Test
       public void testGet() {
           ValueOperations valueOperations = redisTemplate.opsForValue();
           System.out.println("age = " + valueOperations.get("age"));
           System.out.println("username = " + valueOperations.get("username"));
       }
   }
   ```

   注：这里如果使用RedisTemplate而不使用StringRedisTemplate，去redis客户端里面查看会发现键值包含\xac\xed\x00\x05t\x00\特殊字符，这是由于<font color="red">RedisTemplate<K, V>模板类在操作redis时默认使用JdkSerializationRedisSerializer来进行序列化。</font>而存取序列化的方式从`org.springframework.data.redis.serializer.JdkSerializationRedisSerializer`

   将序列化的方式改为 `org.springframework.data.redis.serializer.StringRedisSerializer` 会自动去掉`\xac\xed\x00\x05t\x00`前缀，所以有两种解决方法：

   1. 直接使用StringRedisTemplate；

   2. 方案2 修改默认的序列化方式：

      ```java
      private RedisTemplate redisTemplate;
      @Autowired(required = false)
      public void setRedisTemplate(RedisTemplate redisTemplate) {
          RedisSerializer stringSerializer = new StringRedisSerializer();
          redisTemplate.setKeySerializer(stringSerializer);
          redisTemplate.setValueSerializer(stringSerializer);
          redisTemplate.setHashKeySerializer(stringSerializer);
          redisTemplate.setHashValueSerializer(stringSerializer);
          this.redisTemplate = redisTemplate;
      }
      ```

[P94 实用开发篇-91-SpringBoot读写Redis的客户端](https://www.bilibili.com/video/BV15b4y1a7yG?p=94)

[P95 实用开发篇-92-SpringBoot操作Redis客户端实现技术切换（jedis）](https://www.bilibili.com/video/BV15b4y1a7yG?p=95)

java操作redis底层有两种实现分别为lettuce和jedis，其中lettuce为springboot的RedisTemplate默认使用的技术。如果想要切换到jedis：

1. 引入jedis的jar包

2. 在application.yml中加入配置

   ```yaml
   spring:
     # redis配置
     redis:
       host: 192.168.0.110
       port: 6379
       password: 123456
       client-type: jedis # 默认为lettuce
       # 还可以进一步配置
       jedis:
         pool:
           enabled: true
           max-active: 16
           min-idle: 8
   ```

#### springboot_15_05_mongodb

[P96 实用开发篇-93-Mongodb简介](https://www.bilibili.com/video/BV15b4y1a7yG?p=96)

[P97 实用开发篇-94-Mongodb下载与安装](https://www.bilibili.com/video/BV15b4y1a7yG?p=97)

解压mongodb安装包，然后在软件根目录下新建data\db，进入到bin目录下启动黑窗口，输入如下命令，启动mongodb数据库，并指定数据保存到data\db目录下。

```bash
.\mongod.exe --dbpath=..\data\db
```

在bin目录下再开一个黑窗口，然后输入

```bash
.\mongo.exe
```

会默认连接ip为localhost，port为27017的mongodb服务，连接成功会输出mongodb的版本等信息。

[P98 实用开发篇-95-Mongodb基础操作](https://www.bilibili.com/video/BV15b4y1a7yG?p=98)

由于黑窗口操作较为繁琐，这里推荐使用带图形化界面的客户端robo3t，启动robo3t，创建一个连接

![image-20220125005852352](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125005852352.png)
打开这个连接

![image-20220125005941396](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125005941396.png)

右击左侧连接名，在右键菜单中选择Create Database，新建一个数据库

![image-20220125010258643](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125010258643.png)

填写数据库名称

![image-20220125010907061](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125010907061.png)

展开数据库名，右击Collections再新建一个Collection

![image-20220125011100353](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125011100353.png)

填写collection名称

![image-20220125011142924](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125011142924.png)

右击新建的Collection book，会弹出一个查询界面，可以在文本框中填写指令对Collection book进行操作

![image-20220125011509450](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125011509450.png)

```java
// 查询所有
db.getCollection('book').find({})
// 可以简写为
db.book.find();
// 条件查询
db.book.find({type: "springboot"})

// 保存文档
db.book.save({"name": "springboot", type: "springboot"})

// 删除操作
db.book.remove({type: "springboot"});

// 修改操作
// 修改满足条件的第一条数据
db.book.update({name: "springboot"}, {$set:{name: "springboot2"}});
// 修改满足条件的所有数据
db.book.updateMany({name: "springboot"}, {$set:{name: "springboot2"}});
```

[P99 实用开发篇-96-SpringBoot整合Mongodb](https://www.bilibili.com/video/BV15b4y1a7yG?p=99)

在pom.xml中加入springboot整合MongoDB的依赖

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-mongodb</artifactId>
</dependency>
```

在application.yml中进行MongoDB的配置

```yaml
spring:
  data:
    mongodb:
      uri: mongodb://localhost/springboot_mongodb
```

测试代码

```java
@SpringBootTest
class MongodbApplicationTests {
    @Autowired
    private MongoTemplate mongoTemplate;

    @Test
    void testSave() {
        Book book = new Book();
        book.setId(2);
        book.setName("springboot2");
        book.setType("springboot2");
        book.setDescription("springboot2");
        mongoTemplate.save(book);
    }

    @Test
    public void testFindAll() {
        List<Book> books = mongoTemplate.findAll(Book.class);
        books.forEach(System.out::println);
    }
}
```

#### springboot_15_06_elasticsearch

[P100 实用开发篇-97-ES简介](https://www.bilibili.com/video/BV15b4y1a7yG?p=100)

[P101 实用开发篇-98-ES下载与安装](https://www.bilibili.com/video/BV15b4y1a7yG?p=101)

1. 下载地址：[https://www.elastic.co/cn/start](https://www.elastic.co/cn/start)

2. 安装

   解压es的安装包，然后去bin目录下双击`elasticsearch.bat`启动es服务器，然后就可以去浏览器输入`http://localhost:9200/`

![image-20220125164120683](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125164120683.png)

​		如果有正常的json返回值，那么说明es启动正常

[P102 实用开发篇-99-ES索引操作](https://www.bilibili.com/video/BV15b4y1a7yG?p=102)



1. 安装IK分词器插件

   > 我们希望es再新建索引的时候应用分词效果，所以需要先给es安装IK分词器插件

   下载地址：[https://github.com/medcl/elasticsearch-analysis-ik/releases](https://github.com/medcl/elasticsearch-analysis-ik/releases)

   在es的plugin目录下新建一个ik文件夹（建文件夹是为了方便管理），然后把下载好的ik分词器压缩包中的内容解压到ik目录下

![image-20220125165532370](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125165532370.png)

​		关闭当前es启动的黑窗口，去es的bin目录下，双击`elasticsearch.bat`，重新启动es

2. 新建索引

   打开postman，发送一个PUT请求，新建一个books索引

   请求参数

   ```json
   {
       "mappings": {
           "properties": {
               "id": {
                   "type": "keyword"
               },
               "name": {
                   "type": "text",
                   "analyzer": "ik_max_word",
                   "copy_to": "all"
               },
               "type": {
                   "type": "keyword"
               },
               "description": {
                   "type": "text",
                   "analyzer": "ik_max_word",
                   "copy_to": "all"
               },
               "all": {
                   "type": "text",
                   "analyzer": "ik_max_word"
               }
           }
       }
   }
   ```

![image-20220125182316594](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125182316594.png)

​		返回如下提示就表示新建索引成功

![image-20220125182719019](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125182719019.png)

3. 查询索引

![image-20220125182950127](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125182950127.png)

4. 删除索引

   ![image-20220125192002248](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125192002248.png)

[P103 实用开发篇-100-ES文档操作](https://www.bilibili.com/video/BV15b4y1a7yG?p=103)

1. 新建文档

   有3种请求方式：

   方式1：`http://localhost:9200/books/_doc`

![image-20220125194113251](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125194113251.png)

​		方式2：`http://localhost:9200/books/_doc/221432414`，其中`221432414`是文档中的`_id`属性，如果不指定，则随机生成

![image-20220125205247540](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125205247540.png)

​		方式3：`http://localhost:9200/books/_create/221432414`，其中`221432414`是文档中的`_id`属性，这里不指定会报错

​		![image-20220125203036653](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125203036653.png)

​		注：如果在新建的过程中出现`[TOO_MANY_REQUESTS/12/disk usage exceeded flood-stage watermark, index has read-only-allow-delete block]`的问题，可以发送下面的请求解决

![image-20220125203418217](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125203418217.png)

如果上面的方法也不能解决，检查一下自己的es安装目录所在磁盘的可用空间是否太小，默认必须大于5%才可以，比如磁盘空间500G, 需要至少25G的可用空间才可以。后来清了磁盘大于5%也不行，后来用这个方法解决了：[Elasticsearch flood stage disk watermark exceeded](https://www.hellopp.cn/page/61854946a69f0e0ba433fe39)

2. 查询文档

   * 查询全部文档

   ![image-20220125205830308](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125205830308.png)

   * 查询单个文档

   ![image-20220125205708735](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220125205708735.png)

   * 按条件查询

     ![image-20220126004351659](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126004351659.png)
   
3. 删除文档

   ![image-20220126005031342](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126005031342.png)

4. 修改文档

   将_id为221432414的文档的name修改的值修改为`springboot 非常好`

   先查询一下

   ![image-20220126005606644](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126005606644.png)

   发起请求执行修改操作，这里请求体里面只填写要修改的属性

   ![image-20220126005900814](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126005900814.png)

   再查询一下

   ![image-20220126005941445](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126005941445.png)

   发现修改后的文档，另外两个没有修改的属性没有了，这不是期望的效果，这种请求的修改方式是全覆盖方式的修改。

   如果要想只修改文档中name属性的值，需要使用新的请求方式（操作之前先将_id为221432414的文档数据恢复一下）

   注意：<font color="red">这里发送的是POST请求，而上面的全量修改发送的是PUT请求</font>

   ![image-20220126011856475](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126011856475.png)

   修改之后再查询一下

   ![image-20220126011948653](https://gitee.com/CandyWall/my_pic/raw/master/image/image-20220126011948653.png)

[P104 实用开发篇-101-SpringBoot整合ES客户端操作](https://www.bilibili.com/video/BV15b4y1a7yG?p=104)

[P105 实用开发篇-102-添加文档](https://www.bilibili.com/video/BV15b4y1a7yG?p=105)

[P106 实用开发篇-103-查询文档](https://www.bilibili.com/video/BV15b4y1a7yG?p=106)

参考整合h2、redis、mongodb的方式，整合es的时候应该先在pom.xml中加入spring整合es的依赖，`spring-boot-starter-data-elasticsearch`，然后再去application.yml中编写es的配置，最后再去测试类里面注入es的template对象，进行相关操作。可是需要注意的是，springboot整合es有两套整合方案，一个是整合低级别的es客户端，另一个是整合高级别的es客户端。而开头所说的是springboot整合低级别的方式，这里不采用这种方式。直接整合高级别的es客户端，分为以下几个步骤：

1. 在pom.xml中加入es的依赖，由于测试的过程中还要用到对象转json字符串，所以这里把json解析的依赖也一同加上

    ```xml
    <dependency>
        <groupId>org.elasticsearch.client</groupId>
        <artifactId>elasticsearch-rest-high-level-client</artifactId>
    </dependency>
    <dependency>
        <groupId>com.fasterxml.jackson.core</groupId>
        <artifactId>jackson-databind</artifactId>
    </dependency>
    ```

2. 整合高级别的es客户端，意味着springboot没有提供默认的配置，所以就不能在application.yml中配置有关访问es客户端的url等参数了，这里直接编写测试类，采用硬编码的方式指定这些参数。

   ```java
   @SpringBootTest
   class ElasticsearchApplicationTests {
   //    @Autowired
   //    private ElasticsearchRestTemplate esTemplate;
       @Autowired
       private BookMapper bookMapper;
       private RestHighLevelClient client;
       // json转换工具
       private static ObjectMapper objectMapper;
   
       @Test
       public void testConnect() throws IOException {
           HttpHost host = HttpHost.create("http://localhost:9200");
           RestClientBuilder builder = RestClient.builder(host);
           client = new RestHighLevelClient(builder);
   
           client.close();
       }
   
       @Test
       // 创建索引
       public void testCreateIndex() throws IOException {
           CreateIndexRequest request = new CreateIndexRequest("books");
           client.indices().create(request, RequestOptions.DEFAULT);
       }
   
       @Test
       // 使用IK分词器创建索引
       public void testCreateIndexByIK() throws IOException {
           CreateIndexRequest request = new CreateIndexRequest("books");
           // 设置请求参数
           String jsonParam = "{\n" +
                   "    \"mappings\": {\n" +
                   "        \"properties\": {\n" +
                   "            \"id\": {\n" +
                   "                \"type\": \"keyword\"\n" +
                   "            },\n" +
                   "            \"name\": {\n" +
                   "                \"type\": \"text\",\n" +
                   "                \"analyzer\": \"ik_max_word\",\n" +
                   "                \"copy_to\": \"all\"\n" +
                   "            },\n" +
                   "            \"type\": {\n" +
                   "                \"type\": \"keyword\"\n" +
                   "            },\n" +
                   "            \"description\": {\n" +
                   "                \"type\": \"text\",\n" +
                   "                \"analyzer\": \"ik_max_word\",\n" +
                   "                \"copy_to\": \"all\"\n" +
                   "            },\n" +
                   "            \"all\": {\n" +
                   "                \"type\": \"text\",\n" +
                   "                \"analyzer\": \"ik_max_word\"\n" +
                   "            }\n" +
                   "        }\n" +
                   "    }\n" +
                   "}";
           request.source(jsonParam, XContentType.JSON);
           client.indices().create(request, RequestOptions.DEFAULT);
       }
   
       @Test
       public void testCreateDoc() throws Exception {
           Book book = bookMapper.selectById(1);
   
           IndexRequest request = new IndexRequest("books").id(book.getId() + "");
           String jsonParams = objectMapper.writeValueAsString(book);
           request.source(jsonParams, XContentType.JSON);
           client.index(request, RequestOptions.DEFAULT);
       }
   
       @Test
       // 将mysql数据库tbl_book表中的数据都存到es中
       public void testCreateDocAllFromMySQL() throws Exception {
           List<Book> books = bookMapper.selectList(null);
           // 批处理请求，相当于一个request容器，可以把单个请求加进来
           BulkRequest requests = new BulkRequest();
           for (Book book : books) {
               IndexRequest request = new IndexRequest("books").id(book.getId() + "");
               String jsonParams = objectMapper.writeValueAsString(book);
               request.source(jsonParams, XContentType.JSON);
               requests.add(request);
           }
           client.bulk(requests, RequestOptions.DEFAULT);
       }
   
       @Test
       // 按ID查询
       public void testGet() throws IOException {
           GetRequest request = new GetRequest("books", "1");
           GetResponse response = client.get(request, RequestOptions.DEFAULT);
           System.out.println("book:" + response.getSourceAsString());
       }
   
       @Test
       public void testSearch() throws IOException {
           SearchRequest request = new SearchRequest("books");
   
           SearchSourceBuilder builder = new SearchSourceBuilder();
           builder.query(QueryBuilders.termQuery("all", "spring"));
           request.source(builder);
   
           SearchResponse response = client.search(request, RequestOptions.DEFAULT);
           SearchHits hits = response.getHits();
           for (SearchHit hit : hits) {
               System.out.println(hit.getSourceAsString());
           }
       }
   
       @BeforeEach
       void setUp() {
           objectMapper = new ObjectMapper();
           HttpHost host = HttpHost.create("http://localhost:9200");
           RestClientBuilder builder = RestClient.builder(host);
           client = new RestHighLevelClient(builder);
       }
   
       @AfterEach
       void tearDown() throws IOException {
           client.close();
       }
   }
   ```

### 16. 整合第三方技术

[P107 实用开发篇-104-缓存的作用](https://www.bilibili.com/video/BV15b4y1a7yG?p=107)

[P108 实用开发篇-105-Spring缓存使用方式](https://www.bilibili.com/video/BV15b4y1a7yG?p=108)

[P109 实用开发篇-106-手机验证码案例-生成验证码](https://www.bilibili.com/video/BV15b4y1a7yG?p=109)

[P110 实用开发篇-107-手机验证码案例-验证码校验](https://www.bilibili.com/video/BV15b4y1a7yG?p=110)

[P111 实用开发篇-108-变更缓存供应商Ehcache](https://www.bilibili.com/video/BV15b4y1a7yG?p=111)

[P112 补 知识加油站-04-数据淘汰策略](https://www.bilibili.com/video/BV15b4y1a7yG?p=112)

[P113 实用开发篇-109-变更缓存供应商Redis](https://www.bilibili.com/video/BV15b4y1a7yG?p=113)

[P114 实用开发篇-110-memcached下载与安装](https://www.bilibili.com/video/BV15b4y1a7yG?p=114)

[P115 实用开发篇-111-变更缓存供应商memcached](https://www.bilibili.com/video/BV15b4y1a7yG?p=115)