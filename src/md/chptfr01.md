# 付録1.lane_planner（調整中）

ベクターマップ用定義？



## lane_rule

|  #   | 項目名                    | 内容                                                         | 単位  | smagv妥当値 |
| :--: | ------------------------- | ------------------------------------------------------------ | :---: | ----------- |
|  1   | Accelerarion              | 停止線やカーブで加速・減速する際の加速度を指定する。（カーブ周辺のwaypointの速度が変化する） | m/s^2 | ？          |
|  2   | Stopline Search Radius    | 経路上で停止線を探索する半径を指定する。                     |   m   | ？          |
|  3   | Number of Zero Ahead      | 停止線の前に置く速度0のwaypointの数を指定する。              |  個   | ？          |
|  4   | Number of Zero Behind     | 停止線の後ろに置く速度0のwaypointの数を指定する。            |  個   | ？          |
|  5   | number_of_smoothing_count | 速度を修正するwaypointの数を指定する。                       |  個   | ？          |





## lane_select



https://autoware.readthedocs.io/en/feature-documentation_rtd/DevelopersGuide/PackagesAPI/mission/lane_planner.html

|  #   | 項目名                                | 内容                                                         | 単位 | smagv妥当値 |
| :--: | ------------------------------------- | ------------------------------------------------------------ | :--: | ----------- |
|  1   | Distance threshold to neighbor lanes  | 現在経路の周りの有効な車線を検出する際のしきい値を表す。このしきい値より遠い距離にある車線は車線として認識しない。 |  m   | ？          |
|  2   | Lane Change Interval After Lane merge | 車線変更を行ったあとに何メートル走ったらまた車線変更を行えるようになるかの値を表す。 |  m   | ？          |
|  3   | Lane Change Target Ratio              | 車線変更を行う予定の車線上の目標点を速度(m/s)に比例した距離で定義する際に使用する値。 目標点探索の起点は車線変更予定の車線上の点において、右折or左折の車線変更フラグを持つ点の最近傍点。 |      | ？          |
|  4   | Lane Change Target Minimum            | 車線変更を行う予定の車線上の目標点までの最低距離を表す。 目標点探索の起点は車線変更予定の車線上の点において、右折or左折の車線変更フラグを持つ点の最近傍点。 |  m   | ？          |
|  5   | Vector Length of Hermite Curve        | 曲線補間に使用しているエルミート曲線（始点と終点を滑らかに結ぶ曲線）のベクトルの大きさを指定する。 |  m   | ？          |
|  6   | Enable Planner dynamical switch       | waypointを動的に書き換えるかどうかを指定する。               |  -   | -           |

