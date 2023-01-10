# wms.egs apiDoc

apiDoc creates a documentation from API descriptions in your source code.

### Documentation: [apidocjs.com](http://apidocjs.com)

### [Live DEMO](http://apidocjs.com/example/)

## Usage

简单的演示代码:

```java
            URL apiURL = new URL(strURL);
            String fileName = "wmszip_";
            File zipFile;
            //创建临时文件，写入下载zip内容
            zipFile = null;
            zipFile = File.createTempFile(fileName, ".zip", new File(outputPath));
            LOGGER.info("zipFile：" + zipFile);

            try {
                FileUtils.copyURLToFile(apiURL, zipFile);
                unzip(zipFile, outputPath+"wmsjson/");
            }
```

Now generate the documentation from `src/` into `doc/`.

```bash
$ apidoc -i src/ -o doc/
```

配置文件的示例:

~~~properties
#zip download url
apiURL=https://kubota-wms.egyun.com.cn/pda/api/Interface/DownloadInterfaceData?tocken=************
outputPath=c:/local_data/
~~~


