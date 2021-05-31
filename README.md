一）gazebo8版本

0.先升到gazebo8，可参考下面链接
https://www.codeleading.com/article/99472389135/
1.设置模型位置：
将export GAZEBO_MODEL_PATH=/home/fan/test_ws/src/wheelchair/wheelchair_witharm_description/models(这里写自己的路径)
写入~/.bashrc
source .bashrc
2.需要
catkin_make
source devel/setup.bash
3.使用以下命令加载带有人/机械臂和轮椅的模型
roslaunch wheelchair_witharm_description gazebo.launch 

4.轮椅模型位置
/wheelchair/wheelchair_witharm_description/urdf/wheelchair_with_all.xacro

二）gazebo7版本
0.将/wheelchair/wheelchair_witharm_description/models里的所有文件copy到.gazebo/models下
1.修改
/wheelchair/wheelchair_witharm_description/launch/gazebo.launch
中的第四行
  <arg name="world_file" default="$(find wheelchair_witharm_description)/worlds/small_house.world"/> 
为
  <arg name="world_file" default="$(find wheelchair_witharm_description)/worlds/gazebo7.world"/> 
