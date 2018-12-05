# konwledgePoint
### echart 图表遇到的问题

1、vue 项目 china 地图只显示南海诸岛

解决办法：在main.js 中引入  

```
import echarts from 'echarts'
import 'echarts/map/js/china.js';

```
### vue 打包路径问题
1、注意打包后项目路径是否有二级路径，若有二级路径，则需注意使用相对路径。例如http://aaa.bbb/项目名称
2、config-index.js build模块
```
assetsSubDirectory: 'static',
assetsPublicPath: './',

```
3、build-utils 
```
if (options.extract) {
  return ExtractTextPlugin.extract({
    use: loaders,
    publicPath:'../../',
    fallback: 'vue-style-loader'
  })
  } else {
    return ['vue-style-loader'].concat(loaders)
  }
    
```
3、若资源放在static下，需要请求，则相对路径为@/../static/
