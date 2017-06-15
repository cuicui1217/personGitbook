# 设置项

到这我们的图表就已经出来了，下面就对选项进行说明。

#### option
图表选项，包含图表实例任何可配置选项： 公共选项 ， 组件选项 ， 数据选项
常用的有：
	-公共选项
		-color：表示系列的颜色，可用数组表示，当系列数量个数比颜色列表长度大时将循环选取，上述代码中表示环状百分比图各块的颜色。
	-组件选项
		tooltip：鼠标悬浮交互时的信息提示，即实例图中的黑色浮窗
		legend： 图表块提示，即实例图中最下方的小提示块
	-数据选项
		series：与数据相关，数组中每一项代表一个系列的特殊选项及数据

#### tooltip
提示框，鼠标悬浮交互时的信息提示。
常用的有：
	-trigger：触发类型，默认数据触发，可选为：‘item’ | ‘axis’，实例中为item多用于环状图，axis用于坐标图;
	-formatter: 内容格式器, 有{a}{b}{c}{d}，实例中"{a}<br/>{b}:{c}({d}%)"分别表示： series.data[]中的name值、series.data[]中的value值、环状图每部分的比例

#### series
	-type:
	图表类型，必要参数！如为空或不支持类型，则该系列数据不被显示。可选为：
	‘line’（折线图） | ‘bar’（柱状图） | ‘scatter’（散点图） | ‘k’（K线图）
	‘pie’（饼图） | ‘radar’（雷达图） | ‘chord’（和弦图） | ‘force’（力导向布局图） | ‘map’（地图）
	data：[系列中的数据内容数组](http://echarts.baidu.com/option.html#series-pie.data)
	itemStyle： 标注图形样式属性，通用选项，实例图中为指示线上的内容，在series中有设置（全局），在data中也有设置（为了让当数据为零时隐藏指示线）