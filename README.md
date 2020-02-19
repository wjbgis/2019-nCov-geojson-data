# 2019-nCov  每日累计数据（GeoJson格式）

* 本项目基于[2019-nCoV 全量每日统计数据](<https://github.com/canghailan/Wuhan-2019-nCoV> "访问")，对数据进行清洗、转换生成了geojson格式的每日累计数据，以便于GIS相关项目应用、研究分析使用。

* 数据记录了每天每个城市的确诊、疑似、治愈、死亡累计人数。
* 城市的地理坐标来自于[百度地图web服务API](<https://lbsyun.baidu.com/index.php?title=webapi> "访问")（WGS84坐标，非BD09坐标）。

* 数据不定期更新（争取每日更新一次）。

### 数据示例

```json
{
	"type":"FeatureCollection",
	"features":[
		{
			"type":"Feature",
			"geometry":{
				"type":"Point",
				"coordinates":[114.29955,30.59521]
			},
			"properties":{
				"date":"2020-01-13",
				"country":"中国",
				"province":"湖北省",
				"city":"武汉市",
				"confirmed":41,
				"suspected":0,
				"cured":7,
				"dead":1
			}
		}
	]
}
```

### 属性字段说明

|   date    |   日期   |
| :-------: | :------: |
|  country  |   国家   |
| province  |   省份   |
|   city    |   城市   |
| confirmed | 确诊人数 |
| suspected | 疑似人数 |
|   cured   | 治愈人数 |
|   dead    | 死亡人数 |

### 致谢

感谢[canghailan/Wuhan-2019-nCoV](<https://github.com/canghailan/Wuhan-2019-nCoV> "访问")项目中提供的数据接口。

