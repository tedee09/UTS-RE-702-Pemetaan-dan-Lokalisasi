Nama    : Septedy Indrajannah
NIM     : 4222211006
Matkul  : Lokalisasi dan Pemetaan RE 702

# turtlebot4_nav_uts
Source code UTS RE702

Task dari project ini adalah Robot TurtleBot4 mengantar barang dari Ruang 203 ke Lobby BRAIL di Lantai 2 Gedung Utama Politeknik Negeri Batam secara otonom menggunakan ROS dengan kemampuan lokalisasi, pemetaan, dan navigasi. Sebagai simulasi pengambilan dan pengantaran barang, buzzer berbunyi satu kali saat robot tiba di Ruang 203 dan dua kali saat robot tiba di Lobby BRAIL.

---
# Langkah-langkah dalam menjalankan source code
### Buat Folder Workspace
```
mkdir -p turtlebot4_ws/src
cd turtlebot4_ws/src
```
### Clone Repo 
```
git clone https://github.com//turtlebot4_nav_uts.git
```
### Build 
```
colcon build
```
### Koneksikan PC ke Turtlebot4
```
ssh ubuntu@192.168.185.3 
```
### Jalankan localization launch & navigation launch pada turtlebot4
```
source install/setup.bash
ros2 launch turtlebot4_nav_uts localization.launch.py
```
```
source install/setup.bash
ros2 launch turtlebot4_nav_uts uts_navigation.launch.py
```
### Jalankan Rviz
```
ros2 launch turtlebot4_viz view_robot.launch.py
```
### Jalankan node program pick & place nya yang berisi koordinat awal dan tujuan pada turtlebot4
```
source install/setup.bash
ros2 run turtlebot4_nav_uts koordinat_node
```
