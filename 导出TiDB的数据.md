导出TiDB的数据

下载导出工具

```
tiup install dumpling
```



启动tidb

```
tiup playground --tag tidb_test
```

```
tiup client
```



```
tiup dumpling \
  -u root \
  -h 127.0.0.1 \
  -P 4000 \
  -B cve_db \
  --filetype sql \
  -F 256MiB \
  -o ./dump_cve_db \
  --threads 4
```

![image-20250608013413620](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20250608013413620.png)

![image-20250608013429328](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20250608013429328.png)

打包

```
tar -czvf dump_cve_db.tar.gz ./dump_cve_db
```

