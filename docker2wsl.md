# Docker Container to WSL Distro

```bash
docker pull $OS_IMAGE

docker run -itd --name $CONTAINER_NAME $OS_IMAGE

docker [container] export > "$EXPORT_PATH/$CONTAINER_NAME.tar" $CONTAINER_NAME

wsl --import $DISTRO_NAME $DISTRO_PATH "$EXPORT_PATH/$CONTAINER_NAME.tar"

wsl -d $DISTRO_NAME

wsl -s $DISTRO_NAME

wsl --unregister $DISTRO_NAME
```

## Ubuntu 22.04

```bash
cd "C:\Devel"

docker pull ubuntu:22.04

docker run -itd --name ubuntu2204 ubuntu:22.04

docker export > ubuntu2204.tar ubuntu2204

wsl --import ubuntu2204 "C:\Devel\ubuntu2204" ubuntu2204.tar

wsl -d ubuntu2204

wsl -s ubuntu2204

wsl --unregister ubuntu2204
```

## Centos 7

```bash
cd "C:\Devel"

docker pull centos:7

docker run -itd --name centos7 centos:7

docker export > centos7.tar centos7

wsl --import centos7 "C:\Devel\centos7" centos7.tar

wsl -d centos7

wsl -s centos7

wsl --unregister centos7
```

## Centos 8

```bash
cd "C:\Devel"

docker pull centos:8

docker run -itd --name centos8 centos:8

docker export > centos8.tar centos8

wsl --import centos8 "C:\Devel\centos8" centos8.tar

wsl -d centos8

wsl -s centos8

wsl --unregister centos8
```

## RockyLinux 8

```bash
cd "C:\Devel"

docker pull rockylinux:8

docker run -itd --name rocky8 rockylinux:8

docker export > rocky8.tar rocky8

wsl --import rocky8 "C:\Devel\rocky8" rocky8.tar

wsl -d rocky8

wsl -s rocky8

wsl --unregister rocky8
```

## RockyLinux 9

```bash
cd "C:\Devel"

docker pull rockylinux:9

docker run -itd --name rocky9 rockylinux:9

docker export > rocky9.tar rocky9

wsl --import rocky9 "C:\Devel\rocky9" rocky9.tar

wsl -d rocky9

wsl -s rocky9

wsl --unregister rocky9
```