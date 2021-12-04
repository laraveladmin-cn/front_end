#### 安装前准备

1. 提前安装好git(整套部署流程使用git方式部署,请依照文档通过git clone命令安装

2. Windows环境请进入git bash命令行工具进行执行安装
   
![进入git bash](https://www.laraveladmin.cn/storage/uploads/images/2020/12/09/DCVTN13VC08tcVTBGtpYB0xzCrhMf1Gq9DNKfEPl.png)

3. 安装好nodejs,cnpm(用于前端模板打包编译

> 安装cnpm

```shell
npm install -g cnpm --registry=https://registry.npm.taobao.org
cnpm -v
```

#### 安装

1. 下载前端代码

```shell
git clone https://gitee.com/laravel-admin/front_end.git
cd front_end
cnpm install
```

2. 软连接对应关系

2.1 windows系统执行

```shell
ln -s `pwd`/resources/less/variables.less `pwd`/node_modules/admin-lte/build/less/variables.less  #主题配色变量

ln -s `pwd`/node_modules/animate.css/animate.min.css `pwd`/public/bower_components/animate.css/animate.min.css  #动画样式
ln -s `pwd`/node_modules/bootstrap/dist `pwd`/public/bower_components/bootstrap/dist   #bootstrap静态资源
ln -s `pwd`/node_modules/bootstrap-colorpicker/dist `pwd`/public/bower_components/bootstrap-colorpicker/dist #bootstrap颜色选择器静态资源
ln -s `pwd`/node_modules/echarts/dist `pwd`/public/bower_components/echarts/dist   #echarts图表静态资源
ln -s `pwd`/node_modules/editor.md `pwd`/public/bower_components/editor.md   #editor.md编辑器静态资源
ln -s `pwd`/node_modules/font-awesome `pwd`/public/bower_components/font-awesome 
ln -s `pwd`/node_modules/select2/dist `pwd`/public/bower_components/select2/dist  
ln -s `pwd`/node_modules/xlsx/dist `pwd`/public/bower_components/xlsx/dist
ln -s `pwd`/node_modules/ionicons/dist `pwd`/public/bower_components/ionicons  

ln -s `pwd`/resources/sass/_variables.scss `pwd`/resources/theme/_variables.scss   #主题
ln -s `pwd`/resources/js/components/echarts.theme.json `pwd`/resources/theme/echarts.theme.json 
ln -s `pwd`/resources/less/variables.less `pwd`/resources/theme/variables.less 
```

2.2 linux系统执行
```shell
ln -s ../../../../resources/less/variables.less `pwd`/node_modules/admin-lte/build/less/variables.less  #主题配色变量

ln -s ../../../node_modules/animate.css/animate.min.css `pwd`/public/bower_components/animate.css/animate.min.css  #动画样式
ln -s ../../../node_modules/bootstrap/dist `pwd`/public/bower_components/bootstrap/dist   #bootstrap静态资源
ln -s ../../../node_modules/bootstrap-colorpicker/dist `pwd`/public/bower_components/bootstrap-colorpicker/dist #bootstrap颜色选择器静态资源
ln -s ../../../node_modules/echarts/dist `pwd`/public/bower_components/echarts/dist   #echarts图表静态资源
ln -s ../../node_modules/editor.md `pwd`/public/bower_components/editor.md   #editor.md编辑器静态资源
ln -s ../../node_modules/font-awesome `pwd`/public/bower_components/font-awesome 
ln -s ../../../node_modules/select2/dist `pwd`/public/bower_components/select2/dist  
ln -s ../../../node_modules/xlsx/dist `pwd`/public/bower_components/xlsx/dist
ln -s ../../node_modules/ionicons/dist `pwd`/public/bower_components/ionicons  

ln -s ../../resources/sass/_variables.scss `pwd`/resources/theme/_variables.scss   #主题
ln -s ../../resources/js/components/echarts.theme.json `pwd`/resources/theme/echarts.theme.json 
ln -s ../../resources/less/variables.less `pwd`/resources/theme/variables.less 
```

3. 编译

```shell
npm run prod
npm run watch
```

3. 配置站点目录根目录至public

4. 修改public/index.html对应的获取配置地址对应域名即可

http://local.laraveladmin.cn/

```html
<script src="http://local.laraveladmin.cn/web-api/open/config?script=AppConfig&amp;time=1638509354" type="application/javascript"></script>
```




