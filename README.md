# echart-skillPoint
echart 图表遇到的问题
## vue 项目 china 地图只显示南海诸岛
解决办法：在main.js 中引入  
```
import echarts from 'echarts'
import 'echarts/map/js/china.js';

```
