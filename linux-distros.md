
# Linux Distros

```bash
adduser qwj
passwd qwj
apt install sudo
usermod -aG sudo qwj
su qwj
```

## debian

```bash
apt update && apt upgrade -y

sed -i.bak 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list.d/debian.sources \

apt update

apt install man-db -y
```

## ubuntu

```bash
apt update  && apt upgrade -y

apt install ca-certificates -y

sed -i 's@//.*archive.ubuntu.com@//mirrors.ustc.edu.cn@g' /etc/apt/sources.list
sed -i 's/security.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
sed -i 's/http:/https:/g' /etc/apt/sources.list

unminimize

apt install man-db
```

## fedora

```bash
yum update -y

# [fedora version >= 39]
sed -e 's|^metalink=|#metalink=|g' \
    -e 's|^#baseurl=http://download.example/pub/fedora/linux|baseurl=https://mirrors.ustc.edu.cn/fedora|g' \
    -i.bak \
    /etc/yum.repos.d/fedora.repo \
    /etc/yum.repos.d/fedora-updates.repo

# [fedora version < 39]
sed -e 's|^metalink=|#metalink=|g' \
    -e 's|^#baseurl=http://download.example/pub/fedora/linux|baseurl=https://mirrors.ustc.edu.cn/fedora|g' \
    -i.bak \
    /etc/yum.repos.d/fedora.repo \
    /etc/yum.repos.d/fedora-modular.repo \
    /etc/yum.repos.d/fedora-updates.repo \
    /etc/yum.repos.d/fedora-updates-modular.repo

dnf install -y man man-pages

for pkg in $(dnf repoquery --installed --qf "%{name}"); 
    do dnf reinstall -qy $pkg; 
done
```

## centos

```bash
```

## redhat ubi

```bash
```

## rocky linux

```bash
```

