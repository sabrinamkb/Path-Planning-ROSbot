# Path-Planning-ROSbot

## 1. Create a new workspace 
```
cd
mkdir -p navi_path_plan/src && cd navi_path_plan
catkin_make
```

## 2. Navigate back to the src directory 
```
cd ~/navi_path_plan/src
mkdir rosbot_mapping
```

## 3. Clone this repository and create the package
```
cd rosbot_mapping
git clone https://github.com/sabrinamkb/Path-Planning-ROSbot.git
catkin_create_pkg navi_pkg roscpp
```

## 4. Build the package again
```
cd ~/navi_path_plan
catkin_make
```
