# 数据清洗<br>
- 缺省值
- log，归一化...
***
- 先去除掉10900, 再使用3σ去除其余异常值

# 特征选取<br>
- 相关性分析
- xgboost，randomforest可以获取特征重要性

# 特征工程<br>
**连续型特征**
- 统计特征
- 时序特征

**目前特征**
- 注册年份

**待检验特征**
- 隐藏特征
- 交叉特征
- 城市id：一线城市，二线城市，三线城市（分箱）
- 注册日期，上牌日期 - 展销日期

**离散特征**
- 品牌id：分组
- 车系id：分组
- 车型id：舍弃
- 车辆颜色：不做处理
- 车辆所在城市id：
- 国别：舍弃
- 厂商类型：不做处理
- 燃油类型：

# 模型选择<br>
- 随机森林
- XGboost
- GBDT+LR
- stacking

# 调研
- 天池
- kaggle

https://blog.csdn.net/CarryLvan/article/details/106797353
偏度，峰度，转为正态分布
[1] I.K. Yeo and R.A. Johnson, "A new family of power transformations to
    improve normality or symmetry." Biometrika, 87(4), pp.954-959,
    (2000).

[2] G.E.P. Box and D.R. Cox, "An Analysis of Transformations", Journal
    of the Royal Statistical Society B, 26, 211-252 (1964).
    
**车系和车型确定，一辆车的几乎所有特征都一样，价格也一样**<br>
**严重长尾（舍弃）：车辆颜色，燃油类型，载客人数, Feature_1, Feature_3,**<br>
**缺省值过多（舍弃）：Feature_4, Feature_7, Feature_10, Feature_15**<br>
**车辆所在城市 id，国标码，国别，厂商所在类型，年款，变速箱，Feature_2, F_6, F_8, F_9,**<br>
**bin:排量**