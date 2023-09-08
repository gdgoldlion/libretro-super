# 此仓库仅用作编译 FBNeo 核心

## 编译指南

1.使用 MSYS2 配置编译环境

2.编译 FBNeo 核心无需安装 Qt 库和 Nvidia CG 库

3.仅同步 FBNeo 核心代码和依赖项即可，其他内容无需同步

## 下载

    ./libretro-fetch.sh fbneo

## 编译

参考如下脚本，强制删除 burn.o，因为编译脚本存在 bug，文件不更新

    rm -f ./libretro-super/libretro-fbneo/src/burn/burn.o
    cd  ./libretro-super/libretro-fbneo/src/burner/libretro
    make -f makefile -j8
    mv fbneo_libretro.dll "./target"

## 参考官方文档

https://docs.libretro.com/development/retroarch/compilation/windows/

## 配套 ROM 下载

https://archive.org/details/2020_01_06_fbn
