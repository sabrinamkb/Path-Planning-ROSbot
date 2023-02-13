# Path-Planning-ROSbot

## 1. Create a separate workspace and clone the package by running each command individually on the terminal
```
mkdir -p ~/path_plan/src/
cd ~/path_plan/src
git clone https://github.com/sabrinamkb/Path-Planning-ROSbot.git
cd ..
catkin_make 
source devel/setup.bash
```

## 2. Open a terminal and run the following commands
```
cd ~/path_plan/src/tutorial_pkg
roslaunch rosbot_ekf all.launch
```
