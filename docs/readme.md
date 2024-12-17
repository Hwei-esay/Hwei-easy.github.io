# 一些教程和报错
## 1.在Mkcos中显示公式
[cnblogs教程](https://www.cnblogs.com/searchstar/p/18303613)
:向`mkdocs.yml`中添加：
```
markdown_extensions:
  - pymdownx.arithmatex

extra_javascript:
  - https://cdn.jsdelivr.net/npm/mathjax@2/MathJax.js?config=TeX-AMS-MML_HTMLorMML
```

## 2.在Mkdocs中显示删除线
在Mkdocs中使用`~~哈哈哈~~`格式没有效果：
~~哈哈哈~~

但是可以使用`<del>哈哈哈</del>`可以显示删除线：<del>哈哈哈</del>

## 3.在Mkdocs中显示图片
```
![image](https://images.unsplash.com/photo-1554310603-d39d43033735?q=80&w=2670&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
```
![image](https://images.unsplash.com/photo-1554310603-d39d43033735?q=80&w=2670&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
### 本地图源：
```
![](/assets/nn456.png)
```
<img src="/assets/nn456.png" width = "300" height = "300" div align=center />


> **Tip**
> 使用本地图源时的文件路径是以`\docs`文件夹为源头的，所以文件需要放到这个文件夹下面才能找到。文件目录如下：
``` 
-physics  
--docs  
---assets  
----nn456.png  
--mkdocs.yml  
```

### Unsplash图源：  
![image](https://images.unsplash.com/photo-1646194314870-6e25f74e6e60?q=80&w=2670&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

### 知乎图源：  
![](https://pic1.zhimg.com/v2-e4264a18b37a78221ced72dc01539d98_1440w.jpg)

### bilibili图源：  (无法显示)

```
![]https://i0.hdslb.com/bfs/new_dyn/3f19aa1b7649f33711acb3af89a93d311036847356.png@560w_560h_1e_1c.avif
```

![](https://i0.hdslb.com/bfs/new_dyn/3f19aa1b7649f33711acb3af89a93d311036847356.png@560w_560h_1e_1c.avif)

#### 解决方案：
使用图床（目前使用chrome上的[bilibili图床插件](https://chromewebstore.google.com/detail/bilibili%E5%9B%BE%E5%BA%8A/aofnmlfiomopkmgdngoehlndjcinbhfb)），将图片下载到本地再上传到图床就有图片的url可用。

但是bilibili的图片很大部分使用的是`.webp`或`.avif`格式，还需要多一步将这些格式转换为`.jpg`或`.png`文件

## 4.报错“found character '\t' that cannot start any token”

原因是在`.yaml`文件中不能使用`tab`键进行缩进。

## 5.latex公式无法显示

原因可能是在mkdocs中，<>中的反括号前需要加\，且每一个都要加。

## 6.如何显示Tips、Note、Warning等**块**
具体的规则是：`!!!`+`space`+`Tip`或`Note`或`Warning`。内容文字需要在下一行与`Tip`等缩进相同的位置开始书写。

例如：
```
!!! Tip
    这是一个Tip。
```

!!! Tip
    这是一个Tip。
