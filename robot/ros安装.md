# ros2安装

```bash
不同ubuntu版本的ROS2版本对应表见资料1


#查看系统发行版本
cat /etc/issue

#安装必备的工具
sudo apt update && sudo apt install curl gnupg lsb-release

#添加ROS2软件源的GPGkey
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg


#添加ROS2软件源
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

#更新软件包信息
sudo apt update


#安装完整版
sudo apt install ros-$ROS_DISTRO-desktop


#初始化环境
source /opt/ros/$ROS_DISTRO/setup.bash
```







资料1：https://blog.csdn.net/qq_34802028/article/details/127874424



资料2：https://mp.weixin.qq.com/s?__biz=MzU1NjEwMTY0Mw==&mid=2247555708&idx=2&sn=55b2fbc07a213d22897026f6fc484ab9&chksm=fbc86318ccbfea0e12e6f9a5e04b17cc9ad63b62965bc3ef8e99aa24ece0913e1450b39d8bcc&scene=27



如果遇到The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 

则参考资料2的源增加方式



# ros1安装

ros1安装：https://zhuanlan.zhihu.com/p/498742111

# 参考资料

ros系列文章：http://www.guyuehome.com/3316

ros2常用指令：https://blog.csdn.net/aibingjin/article/details/123899829



ros1安装：https://zhuanlan.zhihu.com/p/498742111

ros入门21讲：https://blog.csdn.net/g944468183/article/details/123844539