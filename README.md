# HYLee_ML2017HW4
李宏毅老師，機器學習，2017作業4，以RNN實作評論情緒分類，以及Semi-supervised learning。
[原始說明檔案](https://docs.google.com/presentation/d/1HnyZowEamy8N4cUT0gY4aoRZuBTluIuoe8uYQdFxhI0/edit#slide=id.p)

### 初步結果
將training data, nolabel data, testing data全部的文字都一起訓練word2vec。<br>
word2vec參數為200個維度，skip-gram，window為3，min_count=1。<br>
<br>
建立Stack LSTM，2層，input_dim為200維，output 1個neuron，通過sigmoid function產生的機率分佈。<br>
fit資料集時，將training中的短句子補滿（最長37個字）。testing時最長有39個字，但只取前37個字。<br>
<br>
目前LeaderBoard上分數：Public=0.80324，Private=0.80117，通過Strong Baseline。<br>
