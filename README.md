gbdt
====

GBDT:Gradient Boosting Decision Tree implemented by golang.<br/>

#Characteristic
Concurrency:Implementing local cocurrent with goroutine when building single tree at each iteration.<br/>
Support missing feature value.Every node in the tree has a child named "UNKNOWN VALUE".So every tree is the ternary tree<br/> 

#Data format
1 1 0:1.1446 1:2 2:35 3:0 4:206.0 ....<br/>
weight label featureid:feature_value....<br/>

#Parameter
All gbdt parameter define in config.go.

Number_of_feature:Feature dimensions.eg:In example/train.data,there are 17 different features.

Max_depth:The maximal depth of the tree. 

Tree_count:Tree count ,namely  iteration numbers.

Shrinkage:Step size.

Feature_sampling_ratio:Feature sample ratio for build tree.

Data_sampling_ratio:Data sample ration for build tree.

Min_leaf_size:Minimal number of samples in leaf.

Losstype :Loss function type,eg least square,log likehood

Debug :Print some debug info.
