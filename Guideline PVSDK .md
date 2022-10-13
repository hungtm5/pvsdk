# Guideline PVSDK

```java
PVCBAuth().apply {
			build(this@MainActivity, object : PVCBAuthListener{
				override fun onError(message: String) {
					Log.d("ERROR", "")
				}
				
				override fun onSuccess(message: String) {
					Log.d("SUCCESS", "")
				}
			})
			startRegister()
		}
```

thêm repo file vào root app và cấu hình gradle (project)

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