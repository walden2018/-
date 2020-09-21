# predictor
##接口
predictor（pre_block, graph_full）
**参数**
**pre_block:** list[graph_full], 要预测的当前block的所有前置block的拓扑结构
**graph_full:** list[[]], 当前预测的block的拓扑结构
**返回**
list[[]], 返回参数graph_full每个节点的操作配置

##graph_full说明
graph_full用领接表来表示图的拓扑结构，这里关键的是对节点的编码方式，首先确定主链，主链是从输入节点到输出节点的最长路径，先对主链进行编码，再对各支链编码。如：[[1,2],[2,5],[3],[4],[],[4]]表示主链长度为5

