简要步骤：
 
#安装git工具

sudo apt install git
 
#使用git命令克隆到指定目录下

git clone https://github.com/coreemu/core
 
#安装系统软件包

sudo apt-get update -y

sudo apt-get install -y ca-certificates git sudo wget tzdata libpcap-dev libpcre3-dev \
    libprotobuf-dev libxml2-dev protobuf-compiler unzip uuid-dev iproute2 iputils-ping \
    tcpdump
 
#添加 Visual Studio Code 的软件包源
sudo apt install software-properties-common apt-transport-https wget

wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"

 
#安装 Visual Studio Code
sudo apt install code
 
#更新pip

sudo apt install python3 python3-pip
 
code core
 
#进入core，执行shell脚本

cd core 

./setup.sh

 
#使用invoke安装相关工具，他的指向是task.py,里面的脚本会自动安装。

inv install
