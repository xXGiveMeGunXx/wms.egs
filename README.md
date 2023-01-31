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

取得文件包示例:

```
+-- wmszip_xxxxxxxxxxxx.zip
|   +-- StockIn_20230131_10.json
|   +-- StockOut_20230131_10.json
|   +-- StockSum_20230131_10.json
```


<table class="have-children-table"><thead><tr><th></th> <th>属性</th> <th>类型</th> <th>说明</th> <th>最低版本</th></tr></thead> <tbody><tr><td><i class="toggle-children-table"></i></td> <td>brand</td> <td>string</td> <td>设备品牌</td> <td><a href="../../../framework/compatibility.html">1.5.0</a></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>model</td> <td>string</td> <td>设备型号。新机型刚推出一段时间会显示unknown，微信会尽快进行适配。</td> <td></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>pixelRatio</td> <td>number</td> <td>设备像素比</td> <td></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>screenWidth</td> <td>number</td> <td>屏幕宽度，单位px</td> <td><a href="../../../framework/compatibility.html">1.1.0</a></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>screenHeight</td> <td>number</td> <td>屏幕高度，单位px</td> <td><a href="../../../framework/compatibility.html">1.1.0</a></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>windowWidth</td> <td>number</td> <td>可使用窗口宽度，单位px</td> <td></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>windowHeight</td> <td>number</td> <td>可使用窗口高度，单位px</td> <td></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>statusBarHeight</td> <td>number</td> <td>状态栏的高度，单位px</td> <td><a href="../../../framework/compatibility.html">1.9.0</a></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>language</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr> </tbody></table>
