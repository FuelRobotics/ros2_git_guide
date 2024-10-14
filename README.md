# ros2_git_guide
ubuntu22.04
천천히 순서대로만 진행해주세요.

## 1. 패키지 만들기
### 1.1 워크스페이스 설정
```sh
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
```
### 1.2 ROS2 패키지 생성 (in the src folder)
```sh
ros2 pkg create <패키지이름> --build-type ament_cmake
```
### 1.3 패지키 빌드 
```sh
cd ~/ros2_ws/
colcon build
```
## 2. 패지키를 깃으로 업로드하기
### 2.1 Git 리포지토리 초기화
```sh
cd ~/ros2_ws/src/<패키지이름>
git init
```
### 2.2 Github 리포지토리 연결
```sh
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
```
### 2.3 Git에 커밋하여 푸시 ("commit"=원하는 이름 변경가능 ex) version1, version2..)
```sh
git add .
git commit -m "commit"
git push -u origin main
```
## 3. Git에 있는 패키지 불러오기 (*항상 src폴더 안에서 아래 git clone을 진행)
```sh
git clone https://github.com/<your-username>/<your-repo-name>.git
cd ~/ros2_ws/
colcon build
```

| Ubuntu | ROS 1 | ROS 2 |
| ------ | ----- | ----- |
| Ubuntu 22.04<br>EOL: April 2027[^4] | - | Humble<br>EOL: May 2027 |
