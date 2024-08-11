# bt-uninstall

## 概述

`bt-uninstall` 是一个用于完全卸载宝塔面板（BT面板）的脚本。默认的宝塔卸载脚本 **无法** 彻底清除面板，会留下残余文件。本项目旨在解决这些问题，确保卸载过程彻底干净。下方为宝塔官方的卸载脚本：

```bash
echo "1) 卸载宝塔"  
echo "2) 卸载宝塔及运行环境(可能影响站点、数据库及其他数据)"
#echo "3) 卸载宝塔及运行环境并清除所有站点相关数据"
echo "*请检查安全类软件是否关闭，否正可能导致无法正常卸载 "
echo "================================================="
read -p "请选择你要进行的操作(1-2 默认:1): " action;
```

他竟然注释掉了第三条选项？！这简直是太不负责任了！所以我决定改进这个卸载脚本，以便于彻底的卸载掉宝塔面板！

## 使用方法

```bash
wget -O bt-uninstall.sh https://raw.githubusercontent.com/zhboner/bt-uninstall/main/bt-uninstall.sh
```

## 功能

- **彻底卸载**：完全移除宝塔面板，包括相关的文件和配置。
- **可选操作**：提供不同的卸载选项，根据需要选择卸载宝塔面板或同时卸载其运行环境。
