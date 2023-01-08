# kernel-X556UQK
适用于ASUS X556UQK系列笔记本电脑的Gentoo 5.18.80内核软硬件配置

## 使用方法
```bash
# emerge --ask sys-kernel/gentoo-sources
```
安装gentoo-sources之后，就可以用仓库中的config替换`/usr/src/linux/.config`文件直接编译

## 可用设备：
- 网卡：Qualcomm Atheros QCA9565 ->   ath9k
- 声卡：Intel Gernic             ->   snd_hda_intel
- 集显：Intel HD Graphics 620    ->   i915
- 独显：Gerforce 940MX           ->   没有配置驱动但是内核默认开放了vfio直通通道
- PCI控制器：Intel Gernic        ->   pcieport
- 以太网络：Realtek RTL8xxx      ->    r8169
