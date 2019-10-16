# Rossman-Predict
Rossman Store Predict
项目步骤
1. 数据预处理
2. 特征选择
   a. 相关性分析
   b. XGBoost基准模型
3. Stacking模型
   一层模型
   a. 随机森林（Random Forest）
   b. ExtraTreesRegressor
   c. AdaBoost
   d. XGBoost（此处用的是2中XGBoost的基准模型）
   二层模型：用的是XGBoost模型
4. 区间模型
   a. 5-9月数据集的XGBoost模型
   b. 1-4月数据集的XGBoost模型
   c. 10-12月数据集的XGBoost模型
   d. 集成模型：对a、b、c的测试集预测值求加权平均
5. 最终集成模型
   最终集成模型：把3中的测试集的预测值加入4中的集成模型中，分配权重，获得最终集成模型
6. 结果验证：包括随机门店预测值结果可视化

