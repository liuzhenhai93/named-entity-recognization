# named-entity-recognization
在github 上比较有名基于bi lstm+crf 的ner模型实现上做了一处修改。原实现的viterbi解码依赖numpy,模型没法脱离python 使用。   
我把调用numpy 的 viterbi解码改成使用tensorflow 算子。这样一来，整个计算都是在tensorflow 计算图中，在纯 C++ 环境也能使用。   
原始项目 https://github.com/Determined22/zh-NER-TF   
语料来自于https://github.com/liwenzhu/corpusZh
