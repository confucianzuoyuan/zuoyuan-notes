# 1. 电商分类和推荐

数据集：

- [电商数据集](https://tianchi.aliyun.com/dataset/140281)

项目需求：

1. 根据商品信息将商品分类到商品所属的品类。
2. 根据用户的访问、购买以及评论信息等，来给用户推荐商品。

商品详情数据集字段：

- `Item_id`
- `Title`
- `Pict_url`
- `Category`
- `Brand_id`
- `Seller_id`

日志数据集字段：

- `Item_id`
- `User_id`
- `Action`
- `Vtime`

评论数据集字段：

- `Item_id`
- `User_id`
- `feedback`

解决方案：

1.  对数据集进行预处理。采用独热编码（one-hot）、归一化等手段将每个字段的数据进行预处理。具体可采用Python的Numpy、Pandas等库来完成。
2. 使用预处理后的数据集训练神经网络（DNN、CNN、RNN）来预测商品所属分类和预测用户最想购买的商品（推荐系统）。并对比DNN、CNN、RNN这三种神经网络算法的性能。具体可采用Pytorch等深度学习框架来完成。
3. 采用Pandas、MySQL、Hive等数据分析工具来对数据集进行一些统计指标的分析。

# 2. 图片搜索

数据集及以及字段如上。

项目需求：给定一张图片（拍照或者网络图片），搜索图片对应的商品。

解决方案：

1. 对图片数据进行预处理。采用调整图像大小、归一化、数据增强（随机旋转、随机裁剪、随机翻转、改变亮度饱和度、添加噪声等）、图片格式转换等手段对图片数据进行预处理。可以使用PyTorch种的torchvision等库来完成。
2. 训练CNN卷积神经网络来完成需求。
3. 学习各种图片预处理技术。

# 3. 电商风控

数据集：

- [风控数据集](https://tianchi.aliyun.com/dataset/144810)

**项目需求**：近年来，图计算尤其是图神经网络等技术获得了快速的发展以及广泛的应用。

在电商平台上的风险商品检测场景中，黑灰产和风控系统之间存在着激烈的对抗，黑灰产为了躲避平台管控，会蓄意掩饰风险信息，通过引入场景中存在的图数据，可以缓解因黑灰产对抗带来的检测效果下降。

在实际应用中，图算法的效果往往和图结构的质量紧密相关，由于风险商品检测场景中对抗的存在，恶意用户会通过伪造设备、伪造地址等方式，伪造较为“干净”的关联关系。如何能够在这种存在着存在大量噪声的图结构数据中充分挖掘风险信息，是一个十分有挑战性的问题，另外该场景中还存在着黑白样本严重不均衡，图结构规模巨大且异构等多种挑战。

解决方案：

使用图神经网络（GNN）以及图卷积神经网络（GCN）技术。电商风控（风险控制）中使用图神经网络（GNN）的原因主要与其在处理复杂关系和结构化数据方面的优势有关。

1. **复杂关系建模**
	- **用户与商品的关系**：电商平台上的用户与商品之间存在复杂的关系，例如用户的购买历史、浏览行为、评分等。GNN 能够有效地建模这些关系，捕捉用户与商品之间的交互信息。
	- **社交网络影响**：用户的行为往往受到社交网络中其他用户的影响，GNN 可以通过图结构来捕捉这些影响，帮助更好地理解用户行为。
2. **多层次信息融合**
	- **多种数据源**：电商平台通常会收集多种类型的数据，包括用户行为数据、商品特征、交易记录等。GNN 能够将这些异构信息融合在一起，通过图结构进行有效学习。
	- **上下文信息**：GNN 可以考虑用户在不同上下文中的行为，例如在不同时间、不同地点的购买习惯，从而提高风控模型的准确性。
3. **异常检测**
	- **识别异常模式**：GNN 可以帮助识别用户行为中的异常模式，例如异常购买、虚假交易等。通过分析用户与商品之间的关系，可以更容易地发现潜在的欺诈行为。
	- **图嵌入**：通过图嵌入技术，GNN 可以将用户和商品映射到低维空间，从而便于进行聚类和异常检测。
4. **动态更新**
	- **实时更新**：电商环境是动态的，用户行为和商品信息不断变化。GNN 可以有效地处理动态图，实时更新模型，以反映最新的用户和商品关系。
	- **适应性强**：GNN 的结构可以适应新加入的节点（如新用户、新商品），使得风控系统能够快速响应市场变化。
5. **预测能力**
	- **行为预测**：GNN 可以用于预测用户的未来行为，例如购买意图、流失风险等。这些预测可以帮助电商平台采取相应的风控措施。
	- **个性化推荐**：通过分析用户与商品的关系，GNN 还可以提升推荐系统的效果，从而间接提高风控能力。
6. **图卷积网络（GCN）**
	- **有效的特征提取**：图卷积网络是一种常见的 GNN 类型，能够通过卷积操作提取节点特征，并考虑邻居节点的影响，从而增强模型的表达能力。

图神经网络在电商风控中的应用能够有效处理复杂的用户与商品关系，融合多种数据源，实时更新模型，并提高异常检测和行为预测的能力。这些特点使得 GNN 成为电商风控领域的重要工具。
# 4. 金融欺诈

数据集

- [金融欺诈数据集1](https://tianchi.aliyun.com/dataset/171696)
- [金融欺诈数据集2](https://tianchi.aliyun.com/dataset/136254)
- [金融欺诈数据集3](https://tianchi.aliyun.com/dataset/189882)

项目需求：保险反欺诈预测以保险风控为背景，保险是重要的金融体系，对社会发展，民生保障起到重要作用。保险欺诈近些年层出不穷，在某些险种上保险欺诈的金额已经占到了理赔金额的20%甚至更多。对保险欺诈的识别成为保险行业中的关键应用场景。

数据集字段：

|字段名称|中文翻译|
|---|---|
|policy_id|保单编号|
|age|年龄|
|customer_months|客户月数|
|policy_bind_date|保单绑定日期|
|policy_state|保单状态|
|policy_csl|保单责任限额|
|policy_deductable|保单自付额|
|policy_annual_premium|保单年保费|
|umbrella_limit|额外责任限额|
|insured_zip|被保险人邮政编码|
|insured_sex|被保险人性别|
|insured_education_level|被保险人教育水平|
|insured_occupation|被保险人职业|
|insured_hobbies|被保险人爱好|
|insured_relationship|被保险人与投保人的关系|
|capital-gains|资本收益|
|capital-loss|资本损失|
|incident_date|事件日期|
|incident_type|事件类型|
|collision_type|碰撞类型|
|incident_severity|事件严重程度|
|authorities_contacted|联系的执法机构|
|incident_state|事件发生州|
|incident_city|事件发生城市|
|incident_hour_of_the_day|事件发生小时|
|number_of_vehicles_involved|参与车辆数量|
|property_damage|财产损失|
|bodily_injuries|身体伤害|
|witnesses|证人|
|police_report_available|警察报告是否可用|
|total_claim_amount|索赔总金额|
|injury_claim|伤害索赔|
|property_claim|财产索赔|
|vehicle_claim|车辆索赔|
|auto_make|汽车品牌|
|auto_model|汽车型号|
|auto_year|汽车年份|
|fraud|欺诈|

解决方案：

1. 对数据集进行预处理。采用独热编码（one-hot）、归一化等手段将每个字段的数据进行预处理。具体可采用Python的Numpy、Pandas等库来完成。
2. 使用预处理后的数据集训练神经网络（DNN、CNN、RNN）来预测是否出现了金融欺诈。并对比DNN、CNN、RNN这三种神经网络算法的性能。这样可以根据输入的字段数据来预测是否可能为金融欺诈行为。具体可采用Pytorch等深度学习框架来完成。
3. 采用Pandas、MySQL、Hive等数据分析工具来对数据集进行一些统计指标的分析。

# 5. 电商评价

数据集

- [电商评价数据集](https://tianchi.aliyun.com/dataset/140281)

