常用快捷键

PC
Ctrl + alt + delete 可以打开任务管理器
win + r 打开相应程序快捷键
win + q 查找本机功能
win + x 
win + e 打开我的电脑

sublimetext
Ctrl + p 打开搜索界面

TencentDesk
alt + f 查找文件

ubuntu
lsb_release -a 查看系统信息

设置开机自启：
将需要开机自启的APP的快捷方式复制到指定文件夹
指定文件夹：win+r shell:startup 





迭代器：不依赖于索引的迭代取值方式。
出现原因是为了找到一种不依赖索引也能进行迭代取值的方案。
可迭代对象：
1. 只要能被for循环遍历的就是迭代对象，
2. 只要内置__iter__()方法的就可以称为可迭代对象
3. 可以转换为迭代器的对象就可以称为可迭代对象
调用可迭代对象的__iter__()方法就得到一个迭代器，或者说把可迭代对象转为迭代器对象

对于迭代器，调用一次next就可以获取一个结果，当调用完了，就会报错StopIteration
类似于老母鸡，很节省内存资源





/var/log/message

安装wsl

大体的步骤：
1.windows安装显卡最新驱动。  注--如果有必要可以制作C盘快照（未来可以恢复）
2.windows安装wsl 2，并移动到D盘。注--保存tar包，未来可以复制wsl镜像，用缺省版本ubuntu即可，不要用太新的，有一些包会有缺失。
3.wsl内安装cuda  注--选择12.2 或者11.9，会影响tensorflow和pytorch的版本
4. wsl内安装anaconda    注--方便建立不同的python环境
5.1 wsl内安装 tensorflow   选择合适版本
5.2 wsl内安装pytorch        选择合适版本


wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/12.4.0/local_installers/cuda-repo-wsl-ubuntu-12-4-local_12.4.0-1_amd64.deb
sudo dpkg -i cuda-repo-wsl-ubuntu-12-4-local_12.4.0-1_amd64.deb
sudo cp /var/cuda-repo-wsl-ubuntu-12-4-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-4



查看显卡信息
nvidia-smi

tf 
软件：
Python 3.6–3.9
Ubuntu 16.04 或更高版本