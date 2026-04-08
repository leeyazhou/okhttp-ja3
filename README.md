# okhttp3-ja3

okhttp3-ja3

## Getting Started

### Installing

查看最新版本
- okhttp-ja3-shade： [https://mvnrepository.com/artifact/com.github.leeyazhou/okhttp-ja3-shade](https://mvnrepository.com/artifact/com.github.leeyazhou/okhttp-ja3-shade)
- bctls-jdk18on-ja3-shade： [https://mvnrepository.com/artifact/com.github.leeyazhou/bctls-jdk18on-ja3-shade](https://mvnrepository.com/artifact/com.github.leeyazhou/bctls-jdk18on-ja3-shade)

```xml
<dependency>
  <groupId>com.github.leeyazhou</groupId>
  <artifactId>okhttp-ja3-shade</artifactId>
  <version>4.12.0.1</version>
</dependency>
<dependency>
  <groupId>com.github.leeyazhou</groupId>
  <artifactId>bctls-jdk18on-ja3-shade</artifactId>
  <version>1.82-1</version>
</dependency>
```

### Example

注意包名是 **com.github.leeyazhou.okhttp3.*.**

```java
import java.io.IOException;
import com.github.leeyazhou.okhttp3.OkHttpClient;
import com.github.leeyazhou.okhttp3.Request;
import com.github.leeyazhou.okhttp3.Response;

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

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=leeyazhou/okhttp-ja3&type=Date)](https://star-history.com/#leeyazhou/okhttp-ja3&Date)
