### LSITSD Dataset ###

LSITSD stands for LSI (Intelligent Systems Laboratory) Traffic Sign Dataset. This dataset was created by a merge process of the following traffic sign datasets:

1) German Traffic Sign Detection Benchmark (GTSDB)
2) Belgium Traffic Sign Dataset (BTSD)
3) Tsinghua-Tencent 100K

Note: the link to the dataset will be published soon.

#### Description ####

The merge process was made because the issues of these datasets: GTSDB contains only 600 images for training, BTSD combines every speed limit traffic sign into one class, and Tsinghua-Tencent 100K contains traffic signs only available in China.

The merge process consisted on selecting the most common classes shared between them along with the most required for autonomous driving and ADAS purposes. 
The images that did not contain any of these selected classes were discarded, and the remaining ones were manually labelled; keeping the training and testing set original distribution from each dataset.

This merge generated an unbalenced dataset, because some classes appear more often than others. 
To fix this problem, a data augmentation process was applied using horizontal flips and random image rotations on the less repeated classes. This process is not applied on the classes that are not equal when flipped horizontally, such as direction signs or speed limit signs.

The resulting dataset contains 30 classes, 9,271 images in the training set and 4,811 images in the testing set. The training set contains 22335 traffic sign labels, and the testing set contains 14571 traffic sign labels, adding a total of 22335 labels.

The traffic sign classes available in the dataset are:

- bump
- school_crosswalk
- danger
- give_way
- priority_next_intersection
- give_way_next_intersection
- stop
- priority_road
- no_entry
- no_traffic_both_ways
- dont_turn_left
- dont_turn_right
- dont_turn_U
- speed_limit_20
- speed_limit_30
- speed_limit_40
- speed_limit_50
- speed_limit_60
- speed_limit_70
- speed_limit_80
- speed_limit_100
- speed_limit_120
- go_straight
- go_left
- go_right
- roundabout
- dont_park
- dont_stop
- go_straight_square
- crosswalk
