# Instalando ROS 2 Humble para Ubuntu 22.04
````
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
````
````
sudo apt install software-properties-common
sudo add-apt-repository universe
````
````
sudo apt update && sudo apt install curl -y
export ROS_APT_SOURCE_VERSION=$(curl -s https://api.github.com/repos/ros-infrastructure/ros-apt-source/releases/latest | grep -F "tag_name" | awk -F\" '{print $4}')
curl -L -o /tmp/ros2-apt-source.deb "https://github.com/ros-infrastructure/ros-apt-source/releases/download/${ROS_APT_SOURCE_VERSION}/ros2-apt-source_${ROS_APT_SOURCE_VERSION}.$(. /etc/os-release && echo ${UBUNTU_CODENAME:-${VERSION_CODENAME}})_all.deb"
sudo dpkg -i /tmp/ros2-apt-source.deb
````
````
sudo apt update
````
````
sudo apt upgrade
````
````
sudo apt install ros-humble-desktop
````
````
sudo apt install ros-humble-ros-base
````
````
sudo apt install ros-dev-tools
````
````
source /opt/ros/humble/setup.bash
````
Exemplo do Talker-Listener
````
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
````
Em outro terminal:
````
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_py listener
````
Em outro terminal
````
sudo apt update && sudo apt install -y \
  python3-flake8-docstrings \
  python3-pip \
  python3-pytest-cov \
  ros-dev-tools
````
````
sudo apt install -y \
   python3-flake8-blind-except \
   python3-flake8-builtins \
   python3-flake8-class-newline \
   python3-flake8-comprehensions \
   python3-flake8-deprecated \
   python3-flake8-import-order \
   python3-flake8-quotes \
   python3-pytest-repeat \
   python3-pytest-rerunfailures
````
````
mkdir -p ~/ros2_humble/src
cd ~/ros2_humble
vcs import --input https://raw.githubusercontent.com/ros2/ros2/humble/ros2.repos src
````
````
sudo apt upgrade
````
````
sudo rosdep init
rosdep update
rosdep install --from-paths src --ignore-src -y --skip-keys "fastcdr rti-connext-dds-6.0.1 urdfdom_headers"
````
Em outro terminal:
````
sudo apt install libacl1-dev -y
sudo apt install libasio-dev
````
````
cd ~/ros2_humble/
colcon build --symlink-install
````
Agora, podemos rodar o exemplo talker-listener. Em outro terminal:
````
. ~/ros2_humble/install/local_setup.bash
ros2 run demo_nodes_cpp talker
````
Em outro terminal
````
. ~/ros2_humble/install/local_setup.bash
ros2 run demo_nodes_py listener
````
# Instalando Ardupilot
````
sudo apt-get update
sudo apt-get install git
sudo apt-get install gitk git-gui
````
## Branching e Commiting
````
git checkout master
````
Para criar um branch chamado ardupilot_git_tutorial:
````
git checkout -b ardupilot_git_tutorial
````
Abra o arquivo Tools/GIT_Test/GIT_Success.txt e escreva seu nome no final e salve. Então:
````
git status
````
Você poderá ver o arquivo modificado
````
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
````
````
git add Tools/GIT_Test/GIT_Success.txt
git commit -m 'Tools: added name to GIT_Success.txt'
git push origin HEAD:ardupilot_git_tutorial
````
````
git submodule update --recursive
git submodule init
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
````
