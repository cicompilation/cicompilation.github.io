---
layout: page
---
## xiongbeer/Cobweb 4.1

### Error Message

---------------------

```java
/home/travis/build/xiongbeer/WebVeins/src/test/java/com/xiongbeer/webveins/downloader/HttpClientDownloaderTest.java:[16,38] cannot find symbol 
symbol: method getStatusCode() 
location: variable page of type com.xiongbeer.webveins.utils.Page 
```

### Code Change

---------------------

***src/main/java/com/xiongbeer/webveins/utils/Page.java***

```diff
+ 	public void setStatusCode(int statusCode){
+ 		this.statusCode = statusCode;
+ 	}
	
+ 	public void setHtml(String entity){
+ 		this.html = new Html(entity);
+ 	}
	
+ 	public int getStatusCode(){
+ 		return this.statusCode;
+ 	}
+ }
```