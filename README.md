# okhttp3-ja3

okhttp3-ja3

## Getting Started

### Installing

```xml
<dependency>
  <groupId>com.github.leeyazhou</groupId>
  <artifactId>okhttp-ja3-shade</artifactId>
  <version>4.12.0.0</version>
</dependency>
```

### Example

注意包名是 **ja3.okhttp3.*.**

```java
import java.io.IOException;
import ja3.okhttp3.OkHttpClient;
import ja3.okhttp3.Request;
import ja3.okhttp3.Response;

public class TestOkhttp {

	public static void main(String[] args) throws IOException {
		String url = "https://www.baidu.com";
		OkHttpClient client = new OkHttpClient.Builder().build();
		Request.Builder request = new Request.Builder().url(url);
		try (Response response = client.newCall(request.build()).execute()) {
			System.out.println(response.body().string());
		}
	}
}
```
