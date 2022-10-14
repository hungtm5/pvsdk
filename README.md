# Guideline PVSDK

thêm repo file vào root app và cấu hình gradle (project)

+root app

-+repo

```java
repositories {
        maven { url "https://maven.google.com" }
        jcenter()
        google()
        maven { url "https://jitpack.io" }
        maven { url "${project.rootDir}/repo" }
    }
```

cấu hình gradle (app)

```java
implementation ('com.pvcombank.sdk:pvsdk:0.1.0@aar'){
        transitive = true
    }
```