####                                        Linux-Ubuntu学习

#### 1、ubuntu安装







#### 2、文件系统

```
/根目录
/home/ransibi 二级子目录
/root 一级子目录
/bin  一级子目录
/mmt  一级子目录
/user 一级子目录
/etc  一级子目录
```

linux下没有像Windows盘符的概念，所有的目录结构都是都是挂在一个树下的       

##### （1）用户目录

Linux系统上支持多个用户，每个用户一个目录。用户目录也就是说用户自己的目录，属于二级子目录，放在home下.

特例：超级用户root，/root

#### 3、创建目录和文件

(1)目录操作：

 --- 创建目录

```
mkdir 文件夹名称
```

---创建多层目录

```
mkdir -p 文件夹名称1/文件夹名称2/......
```

---删除目录

```
rmdir 文件夹名称
```

---删除多层目录--强制删除

```
rm -rf 文件夹名称1/文件夹名称2/......
```

---拷贝文件或者目录

```
cp -rf 文件夹1 文件夹2
```

---目录重命名

```
mv 文件夹名称/文件名称   文件夹名称1/文件名称1 
```



#### 4、归档--并没有压缩

tar也就是tape archive档案打包。

(1)创建档案包:

```
tar -cvf 文件夹名称.tar 文件夹名称
```

注意:

  c 表示创建档案

  v 表示显示详情

  f 表示file

也可以多级目录打包:

```
tar -cvf xxx.tar file1 file2 file3
```

(2)还原归档包:

```
tar -xvf 文件夹名称.tar
tar -xvf 文件夹名称.tar -C outdir
其中-C参数指定目标目录，默认解到当前目录
```



#### 5、归档并压缩

```
tar -czvf example.tar.gz example
解压缩
tar -xzvf example.tar.gz
tar -xzvf example.tar.gz -C outdir
```



#### 6、软连接