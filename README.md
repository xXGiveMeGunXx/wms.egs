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

### JSON文件内容

▼StockIn/StockOut文件内容
<table class="have-children-table"><thead><tr><th></th> <th>属性</th> <th>类型</th> <th>说明</th></tr></thead> 
<tbody>
<tr><td><i class="toggle-children-table"></i></td> <td>I_STOCK_INOUT_NO</td> <td>string</td> <td>入出库单号</td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_DETAIL_NO</td> <td>number</td> <td>入出库单明细NO</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_INOUT_TIME</td> <td>date</td> <td>入出库时间</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ITEM_CD</td> <td>string</td> <td>品番</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ITEM_NAME</td> <td>string</td> <td>品名</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ACC</td> <td>number</td> <td>ACC</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_KKONAY</td> <td>number</td> <td>加工内容</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_TAX_KB</td> <td>string</td> <td>保税区分（Y：保税，N：课税）</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_REASON</td> <td>string</td> <td>入出库理由 （区分值一览）</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_QTY</td> <td>number</td> <td>数量</td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_REMARK_D</td> <td>string</td> <td>明细备注</td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_NO</td> <td>string</td> <td>相关单据号</td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_DETAIL_NO</td> <td>string</td> <td>相关单据明细号</td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_NO2</td> <td>string</td> <td>相关单据号2</td></tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ABOUT_RECEIPT_DETAIL_NO2</td> <td>string</td> <td>相关单据明细号2</td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ENTRY_ID</td> <td>string</td> <td></td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_ENTRY_DATE</td> <td>date</td> <td></td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_UPD_ID</td> <td>string</td> <td></td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_UPD_DATE</td> <td>date</td> <td></td> </tr>
<tr><td><i class="toggle-children-table"></i></td> <td>I_CODE</td> <td>string</td> <td>仓库编号</td> </tr>
</tbody>
</table>

▼StockSum文件内容
<table class="have-children-table"><thead><tr><th></th> <th>属性</th> <th>类型</th> <th>说明</th></tr></thead> 
<tbody>
<tr><td><i class="toggle-children-table"></i></td> <td>I_WH_NO</td> <td>string</td> <td>仓库编号</td></tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ITEM_CD</td> <td>string</td> <td>品番</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_ACC</td> <td>number</td> <td>ACC</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_KKONAY</td> <td>number</td> <td>加工内容</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_TAX_KB</td> <td>string</td> <td>保税区分（Y：保税，N：课税）</td> </tr> 
<tr><td><i class="toggle-children-table"></i></td> <td>I_STOCK_QTY</td> <td>number</td> <td>库存数</td> </tr>
</tbody>
</table>

