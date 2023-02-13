# Path-Planning-ROSbot

## 1. Create a new workspace 
```
cd
mkdir -p navi_pathplan/src && cd navi_pathplan
catkin_make
```

## 2. Create a folder in your workspace 
```
cd ~/navi_pathplan/src
mkdir rosbot_mapping
```

## 3. Clone the original Husarion's repository 
```
cd rosbot_mapping
git clone https://github.com/Xedorach/tutorial_pkg.git
```

## 4. Create your package
```
catkin_create_pkg navigation_pkg roscpp
```

## 5. Build your package 
```
cd ~/navi_pathplan
catkin_make
```
