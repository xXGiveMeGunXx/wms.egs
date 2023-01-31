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


<table class="have-children-table"><thead><tr><th></th> <th>属性</th> <th>类型</th> <th>说明</th> <th>最低版本</th></tr></thead> 
<tbody>
<tr><td><i class="toggle-children-table"></i></td> <td>I_STOCK_INOUT_NO</td> <td>string</td> <td>设备品牌</td> <td><a href="../../../framework/compatibility.html">1.5.0</a></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_DETAIL_NO</td> <td>string</td> <td>设备型号。新机型刚推出一段时间会显示unknown，微信会尽快进行适配。</td> <td></td></tr> <tr><td><i class="toggle-children-table"></i></td> <td>I_INOUT_TIME</td> <td>number</td> <td>设备像素比</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ITEM_CD</td> <td>number</td> <td>屏幕宽度，单位px</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ITEM_NAME</td> <td>number</td> <td>屏幕高度，单位px</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ACC</td> <td>number</td> <td>可使用窗口宽度，单位px</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_KKONAY</td> <td>number</td> <td>可使用窗口高度，单位px</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_TAX_KB</td> <td>number</td> <td>状态栏的高度，单位px</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_REASON</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_QTY</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_REMARK_D</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_NO</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_DETAIL_NO</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_NO2</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_DETAIL_NO2</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ENTRY_ID</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ENTRY_DATE</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_UPD_ID</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_UPD_DATE</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_CODE</td> <td>string</td> <td>微信设置的语言</td> <td></td></tr>
</tbody>
</table>
