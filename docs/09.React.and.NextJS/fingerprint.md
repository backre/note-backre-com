
使用这个库：[fingerprintjs](https://github.com/fingerprintjs/fingerprintjs/)

首先下载：

    https://openfpcdn.io/fingerprintjs/v3

并将下载文件改名：

    mv -i v3 fingerprintv3.js

使用方法：

```
import fpPromise from "./fingerpintv3";

    // Get the visitor identifier when you need it.
    const fp = fpPromise.load();

    fp
      .then((fp: any) => fp.get())
      .then((result: any) => {
        const visitorId = result.visitorId;
        console.log('fingerprint: ', visitorId);
      })
      .catch((error: any) => {
        console.error(error);
      });
```

