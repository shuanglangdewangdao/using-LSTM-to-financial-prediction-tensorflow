# using-LSTm-to-financial-prediction
just using kinds of method of neural network to prediction financial market
使用Long Short Term Memory (LSTM)长短期记忆神经网络去预测金融市场价格
使用过去20天的历史数据（开盘价，收盘价，最高价，最低价，交易量）回归预测
raw_data.csv 从Tushare中获取的股票数据
preprocess_data.py对交易量进行归一化，生成stock_data.csv
lstm.py搭建LSTM网络并进行预测，将注释删除可以查看每次训练20次后的预测价格
========================
附输出误差结果（为减少输出数量，以下为50次训练的每次结果，对前200条数据进行预测）：
cost( 0 ):  1393.7227
cost( 50 ):  277.8622
cost( 100 ):  110.7024
cost( 150 ):  40.3059
cost( 200 ):  16.0439
cost( 250 ):  7.7574
cost( 300 ):  7.4863
cost( 350 ):  6.894
cost( 400 ):  6.4133
cost( 450 ):  5.8798
cost( 500 ):  5.3836
cost( 550 ):  4.9585
cost( 600 ):  4.5662
cost( 650 ):  4.2003
cost( 700 ):  3.8922
cost( 750 ):  3.2889
cost( 800 ):  7.7335
cost( 850 ):  7.732
cost( 900 ):  7.7301
cost( 950 ):  7.7355
cost( 1000 ):  7.7288
cost( 1050 ):  7.7337
cost( 1100 ):  7.7281
cost( 1150 ):  7.2338
cost( 1200 ):  6.5705
cost( 1250 ):  3.7096
cost( 1300 ):  3.9418
cost( 1350 ):  3.1127
cost( 1400 ):  2.9791
========================
附预测结果：
cost( 1300 ):  3.8635
pred: 
[[9.200998 ]
 [9.149523 ]
 [9.218034 ]
 [9.331808 ]
 [9.374109 ]
 [9.34836  ]
 [9.278702 ]
 [9.209988 ]
 [9.214067 ]
 [9.2997465]
 [9.294179 ]
 [9.301516 ]
 [9.328058 ]
 [9.313486 ]
 [9.28639  ]
 [9.308395 ]
 [9.342477 ]
 [9.410005 ]
 [9.435549 ]
 [9.426452 ]
 [9.219633 ]
 [9.326253 ]
 [9.345161 ]
 [9.34622  ]
 [9.368155 ]
 [9.373026 ]
 [9.386984 ]
 [9.400506 ]
 [9.40142  ]
 [9.389712 ]
 [9.391174 ]
 [9.278898 ]
 [9.248356 ]
 [9.23941  ]
 [9.138511 ]
 [9.01884  ]
 [8.935734 ]
 [8.909157 ]
 [8.85597  ]
 [8.824619 ]
 [9.186502 ]
 [9.098251 ]
 [9.052919 ]
 [9.046134 ]
 [9.112818 ]
 [9.225739 ]
 [9.263992 ]
 [9.272428 ]
 [9.277512 ]
 [9.275928 ]
 [9.320212 ]
 [9.321854 ]
 [9.327064 ]
 [9.30112  ]
 [9.320164 ]
 [9.320649 ]
 [9.348013 ]
 [9.342398 ]
 [9.328269 ]
 [9.331662 ]
 [9.360127 ]
 [9.320968 ]
 [9.174308 ]
 [9.100613 ]
 [9.06735  ]
 [9.067491 ]
 [9.183535 ]
 [9.284675 ]
 [9.327749 ]
 [9.347467 ]
 [9.366325 ]
 [9.356852 ]
 [9.366522 ]
 [9.386607 ]
 [9.3863125]
 [9.410236 ]
 [9.435661 ]
 [9.430062 ]
 [9.432795 ]
 [9.380736 ]
 [9.321902 ]
 [9.356934 ]
 [9.365471 ]
 [9.373845 ]
 [9.374855 ]
 [9.383278 ]
 [9.387951 ]
 [9.375612 ]
 [9.340731 ]
 [9.323864 ]
 [9.341403 ]
 [9.293842 ]
 [9.272707 ]
 [9.288793 ]
 [9.314037 ]
 [9.333393 ]
 [9.31764  ]
 [9.294747 ]
 [9.280951 ]
 [9.291072 ]
 [8.874701 ]
 [9.104121 ]
 [9.233855 ]
 [9.286295 ]
 [9.181779 ]
 [9.078023 ]
 [9.049849 ]
 [9.061672 ]
 [9.077454 ]
 [9.083578 ]
 [9.092395 ]
 [9.083106 ]
 [9.090661 ]
 [9.07683  ]
 [9.006615 ]
 [8.919616 ]
 [8.819067 ]
 [8.71319  ]
 [8.606607 ]
 [8.547577 ]
 [9.023905 ]
 [8.858309 ]
 [8.699116 ]
 [8.590612 ]
 [8.561141 ]
 [8.667612 ]
 [8.897869 ]
 [9.059434 ]
 [9.177336 ]
 [9.266898 ]
 [9.338984 ]
 [9.343356 ]
 [9.315905 ]
 [9.266764 ]
 [9.231592 ]
 [9.2446   ]
 [9.264102 ]
 [9.237594 ]
 [9.213831 ]
 [9.202648 ]
 [9.118143 ]
 [9.152333 ]
 [9.157772 ]
 [9.059887 ]
 [8.957269 ]
 [8.88685  ]
 [8.894806 ]
 [8.905558 ]
 [8.940718 ]
 [8.974188 ]
 [8.944511 ]
 [8.847059 ]
 [8.750543 ]
 [8.691321 ]
 [8.643199 ]
 [8.651282 ]
 [8.7411175]
 [8.88114  ]
 [9.025127 ]
 [8.998544 ]
 [8.264727 ]
 [8.336608 ]
 [8.3028965]
 [8.339389 ]
 [8.282207 ]
 [8.24995  ]
 [8.204651 ]
 [8.1594925]
 [8.106848 ]
 [8.132615 ]
 [8.120768 ]
 [8.16473  ]
 [8.170663 ]
 [8.185994 ]
 [8.225097 ]
 [8.200307 ]
 [8.144644 ]
 [8.05174  ]
 [8.042845 ]
 [8.034809 ]
 [8.041708 ]
 [8.018602 ]
 [7.9944   ]
 [7.971196 ]
 [7.9575806]
 [7.9751453]
 [8.0176325]
 [8.030065 ]
 [8.081223 ]
 [8.1311245]
 [8.128544 ]
 [8.185853 ]
 [8.300782 ]
 [8.374895 ]
 [8.394728 ]
 [8.40149  ]
 [8.367828 ]
 [8.241876 ]
 [8.128793 ]
 [8.109222 ]]
