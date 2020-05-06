# Github Pages

1.在*setting-GitHub Pages*设置的地方，*source*可以设置为各个分支，或者设置为默认的 *master branch /docs folder* 

2.对仓库对应的gitbook编译

*gitbook build . docs*

编译的资源和html等文件就会在docs文件夹下

如果编译的时候，一直随机报资源找不到错误，改一下配置

 修改 `C:\Users\Administrator\.gitbook\versions\3.2.3\lib\output\website\copyPluginAssets.js` 文件中的 112 行 

```
{
	deleteFirst: false,
	overwrite: true,
	confirm: true
}
```

 将 `confirm: true` 改为 `confirm: false` 

3.编译的文件push到线上，在*setting*页面选择 *master branch /docs folder* 

，刷新的地址打开就可以访问了