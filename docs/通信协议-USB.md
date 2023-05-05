---
id: 通信协议-USB
title: 通信协议 - USB 🚧
---

## USB 版本

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20211129094423.png)

## USB 机械接口

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20211129094855.png)

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20211129094944.png)

接口定义 - 标准 USB：

| 触点 | 功能                 |
| ---- | -------------------- |
| 1    | VBUS（4.75－5.25 V） |
| 2    | D-                   |
| 3    | D+                   |
| 4    | GND                  |

接口定义 - Mini USB：

| 触点 | 功能                 | 颜色 |
| ---- | -------------------- | ---- |
| 1    | VBUS（4.75－5.25 V） | 红   |
| 2    | D-                   | 白   |
| 3    | D+                   | 绿   |
| 4    | ID                   |      |
| 5    | GND                  | 黑   |

## USB 插头与版本的兼容性

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20211129094829.png)

---

## USB Type-C

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20220520105345.png)

### 端口类型

数据：

- **下行端口（Downstream Facing Port，DFP）**：主机 / 下行集线器端口。典型示例为传统的标准 Type-A 端口。
- **上行端口（Upstream Facing Port，UFP）**：设备 / 上行集线器端口。典型示例为传统的标准 Type-B 端口。
- **双重角色端口（Dual-Role Port，DRP）**：连接事件发生前，在 DFP 端口和 UFP 端口之间切换的端口。初始连接事件后，可通过 USB 供电协议协商进行动态交换。

供电：

- **拉电流电源 / 供电设备**：5V-20V 时的拉电流最多为 5A。典型示例为传统的标准 Type-A 端口。
- **灌电流电源 / 耗电设备**：5V-20V 时的灌电流最多为 5A。典型示例为传统的标准 Type-B 端口。

## 引脚定义

Type-C 分公母头（插头与插座），两者引脚大部分呈镜像分布。

Type-C 插座：

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20220520134239.png)

Type-C 插头：

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20220520134304.png)

对接示意图（全功能）：

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20220520140019.png)

引脚定义：

| 引脚 | 名称 | 功能              | 详细说明                                         |
| ---- | ---- | ----------------- | ------------------------------------------------ |
| A1   | GND  | 电源              | 最低支持 60W（与所有 VBUS 结合使用）             |
| A2   | TX1+ | USB3.1 或备用模式 | 与 TX1- 共同构成 10 Gbps 差分对                   |
| A3   | TX1- | USB3.1 或备用模式 | 与 TX1+ 共同构成 10 Gbps 差分对                   |
| A4   | VBUS | 电源              | 最低支持 60W（与所有 VBUS 结合使用）             |
| A5   | CC1  | CC 或 VCONN       | 用于方向检测、电流能力通告检测及 USB2.0 BMC 通信 |
| A6   | D+   | USB2.0            | —                                                |
| A7   | D-   | USB2.0            | —                                                |
| A8   | SBU1 | 备用模式          | 低速边带信号，仅供备用模式使用                   |
| A9   | VBUS | 电源              | 最低支持 60W（与所有 VBUS 结合使用）             |
| A10  | RX2- | USB3.1 或备用模式 | 与 RX2+ 共同构成 10 Gbps 差分对                   |
| A11  | RX2+ | USB3.1 或备用模式 | 与 RX2- 共同构成 10 Gbps 差分对                   |
| A12  | GND  | 电源              | 最低支持 60W（与所有 VBUS 结合使用）             |
| B1   | GND  | 电源              | 最低支持 60W（与所有 VBUS 结合使用）             |
| B2   | TX2+ | USB3.1 或备用模式 | 与 TX2- 共同构成 10 Gbps 差分对                   |
| B3   | TX2- | USB3.1 或备用模式 | 与 TX2+ 共同构成 10 Gbps 差分对                   |
| B4   | VBUS | 电源              | 最低支持 60W（与所有 VBUS 结合使用）             |
| B5   | CC2  | CC 或 VCONN       | 用于方向检测、电流能力通告检测及 USB2.0 BMC 通信 |
| B6   | D+   | USB2.0            | —                                                |
| B7   | D-   | USB2.0            | —                                                |
| B8   | SBU2 | 备用模式          | 低速边带信号，仅供备用模式使用                   |
| B9   | VBUS | 电源              | 最低支持 60W                                     |
| B10  | RX1- | USB3.1 或备用模式 | 与 RX1+ 共同构成 10 Gbps 差分对                   |
| B11  | RX1+ | USB3.1 或备用模式 | 与 RX1- 共同构成 10 Gbps 差分对                   |
| B12  | GND  | 电源              | 最低支持 60W                                     |

供电协议：

| 模式                    | 标称电压 | 最大电流 |
| ----------------------- | -------- | -------- |
| USB2.0                  | 5V       | 500 mA   |
| USB3.0/USB3.1           | 5V       | 900 mA   |
| USB BC1.2               | 5V       | 1.5A     |
| USB Type-C Current @ 1.5A | 5V       | 1.5A     |
| USB Type-C Current @ 2.0A | 5V       | 3.0A     |
| USB PD                  | 最高 20V | 最高 5A  |

### CC 引脚

CC 引脚使用的上下拉电阻取决于是下行端口（DFP）、上行端口（UFP）还是电子标记/有源电缆，必须始终通过端口监视才能实现插入与移除检测、方向检测、电流能力通告的功能。

**主机 / 下行端口（DFP）使用上拉电阻**。上拉电阻 Rp 需同时连接至 CC1 与 CC2 引脚，并上拉至 3.3V/5V/电流源。上拉电阻的取值将向设备通过端口的供电电流能力，如下表所示：

| DFP 供电电流能力                            | 上拉至 4.75V~5.5V | 上拉至 3.3V±5% | 至 1.7~5.5V 电流源 |
| ------------------------------------------- | ----------------- | -------------- | ------------------ |
| 默认 USB 功率（USB2.0-500mA，USB3.0-900mA） | 56kΩ±20%          | 36kΩ±20%       | 80µA±20%           |
| 1.5A@5V                                     | 22kΩ±5%           | 12kΩ±5%        | 180µA±8%           |
| 3A@5V                                       | 10kΩ±5%           | 4.7kΩ±5%       | 330µA±8%           |

**设备 / 上行端口（UFP）使用下拉电阻或电压钳位**。下拉电阻 Rd 的值恒定为 5.1kΩ±10%。

电缆方向检测，如果 CC1 引脚检测到有效的上下拉，则代表正向（未翻转）；如果 CC1 检测到，则代表反向（已翻转）：

![](https://wiki-media-1253965369.cos.ap-guangzhou.myqcloud.com/img/20220520141738.png)

## 参考与致谢

- [USB 相关介绍](https://blog.infonet.io/2020/03/21/USB%E7%9B%B8%E5%85%B3%E4%BB%8B%E7%BB%8D/)
- [USB](https://zh.wikipedia.org/wiki/USB)
- [USB Logo Usage Guidelines](https://www.usb.org/sites/default/files/usb-if_logo_usage_guidelines_final_103019.pdf)
- [AN1953 | USB Type-C™ 简介](http://www.microchip.com.cn/community/Uploads/Download/Library/00001953a_cn.pdf)

> 原文地址：<https://wiki-power.com/>  
> 本篇文章受 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh) 协议保护，转载请注明出处。

