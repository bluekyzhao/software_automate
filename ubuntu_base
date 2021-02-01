# root 安装
cp /etc/apt/sources.list /etc/apt/sources.list.save
sed -i "s@http://cn.archive.ubuntu.com/ubuntu/@http://mirrors.aliyun.com/ubuntu/@g" /etc/apt/sources.list
sed -i "s@http://security.ubuntu.com/ubuntu@http://mirrors.aliyun.com/ubuntu@g" /etc/apt/sources.list

echo "apt update && apt upgrade -y && apt dist-upgrade -y && apt autoremove -y && apt autoclean -y" > ~/000000.sh
chmod 755 ~/000000.sh && sh ~/000000.sh

apt install build-essential vim wget python3.9 python3.9-dev python3.9-venv -y


# user安装
mkdir -p ~/Programs && cd ~/Programs && python3.9 -m venv pyenv39
echo "source ~/Programs/pyenv39/bin/activate" >> ~/.bashrc && source ~/.bashrc
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple
pip install -U pip wheel
