# XC7K325TExpansionBoard
## 〇、关于

### 1 简介

-   为百芯计划中FPGA核心板设计的扩展板

### 2 环境

-   立创EDA专业版（本地）
-   [核心板购买链接](https://item.taobao.com/item.htm?spm=a1z0d.6639537/tb.1997196601.4.6dde7484CnjMZ4&id=715034315098)

### 3 目录

```text
.
├── doc
│   ├── core // 核心板资料
│   │   ├── 7Series_Pkg_Pinout.pdf
│   │   ├── Family_7serial.pdf
│   │   └── XC7K325T.pdf
│   ├── datasheet // 数据手册（有冗余）
│   │   ├── C114425_DC-DC电源芯片-tps5450.pdf
│   │   ├── C132156_USB芯片_USB3320C-EZK-TR_规格书_MICROCHIP(美国微芯)USB芯片规格书.PDF
│   │   ├── C1352196_同步动态随机存取内存(SDRAM)_IS42S16320F-6BLI_规格书_ISSI(美国芯成)同步动态随机存取内存(SDRAM)规格书.PDF
│   │   ├── C1519100_视频接口芯片_SII164CTG64_规格书_LATTICE(莱迪思)预售芯片规格书.PDF
│   │   ├── C24905_排母_1.27-2-50P母_规格书_BOOMELE(博穆精密)排母规格书.PDF
│   │   ├── C296130_监控和复位芯片_HX811R_规格书_HX(恒佳兴)监控和复位芯片规格书.PDF
│   │   ├── C359957_以太网模块_LAN8720+ETH+BOARD_规格书_WAVESHARE(微雪电子)以太网模块规格书.PDF
│   │   ├── C393941_SD卡连接器_TF+PUSH_规格书_SHOU+HAN(首韩)SD卡连接器规格书.PDF
│   │   ├── C45223_以太网芯片_LAN8720A-CP-TR_规格书_MICROCHIP(美国微芯)以太网芯片规格书.PDF
│   │   ├── C55683_以太网连接器(RJ45+RJ11)_HR961160C_规格书_HANRUN(汉仁)以太网连接器(RJ45+RJ11)规格书.PDF
│   │   ├── C6185_线性稳压器(LDO)_AMS1117-1.8_规格书_AMS线性稳压器(LDO)规格书.PDF
│   │   ├── C720616_D-SUB-DVI-HDMI连接器_HDMI-001S_规格书_WJ413945.PDF
│   │   ├── C8734_单片机(MCU-MPU-SOC)_STM32F103C8T6_规格书_ST(意法半导体)单片机(MCU_MPU_SOC)规格书.PDF
│   │   ├── C9006_无源晶振_X322525MOB4SI_规格书_YXC(扬兴晶振)无源晶振规格书.PDF
│   │   ├── C97522_NOR+FLASH_W25Q256JVEIQ_规格书_WINBOND(华邦)NOR+FLASH规格书.PDF
│   │   └── C99652_USB芯片_CH340E_规格书_规格书WJ377529.PDF
│   └── reference // 设计参考
│       ├── 百芯A7-原理图.pdf
│       ├── dvi-12bit-sch.pdf
│       ├── USB2514-HUB.pdf
│       └── ZU15EG_R3_SCH.pdf
├── README.md
└── XC7K325T.eprj // 立创EDA工程

4 directories, 25 files
```

## 一、设计

-   TODO（成功打样并工作后更新）

### 1 SODIMM(144)引脚定义

以下是SODIMM引脚的描述：

| Pin Num (Odd) | Pin Name | Description                   | Pin Num (Even) | Pin Name | Description           |
| ------------: | :------- | :---------------------------- | -------------: | :------- | :-------------------- |
|             1 | Vss      | Ground                        |              2 | Vss      | Ground                |
|             3 | DQ0      | Data line                     |              4 | DQ32     | Data line             |
|             5 | DQ1      | Data line                     |              6 | DQ33     | Data line             |
|             7 | DQ2      | Data line                     |              8 | DQ34     | Data line             |
|             9 | DQ3      | Data line                     |             10 | DQ35     | Data line             |
|            11 | Vdd      | Power supply                  |             12 | Vdd      | Power supply          |
|            13 | DQ4      | Data line                     |             14 | DQ36     | Data line             |
|            15 | DQ5      | Data line                     |             16 | DQ37     | Data line             |
|            17 | DQ6      | Data line                     |             18 | DQ38     | Data line             |
|            19 | DQ7      | Data line                     |             20 | DQ39     | Data line             |
|            21 | Vss      | Ground                        |             22 | Vss      | Ground                |
|            23 | DQM0     | Data mask                     |             24 | DQM4     | Data mask             |
|            25 | DQM1     | Data mask                     |             26 | DQM5     | Data mask             |
|            27 | Vdd      | Power supply                  |             28 | Vdd      | Power supply          |
|            29 | A0       | Address line                  |             30 | A3       | Address line          |
|            31 | A1       | Address line                  |             32 | A4       | Address line          |
|            33 | A2       | Address line                  |             34 | A5       | Address line          |
|            35 | Vss      | Ground                        |             36 | Vss      | Ground                |
|            37 | DQ8      | Data line                     |             38 | DQ40     | Data line             |
|            39 | DQ9      | Data line                     |             40 | DQ41     | Data line             |
|            41 | DQ10     | Data line                     |             42 | DQ42     | Data line             |
|            43 | DQ11     | Data line                     |             44 | DQ43     | Data line             |
|            45 | Vdd      | Power supply                  |             46 | Vdd      | Power supply          |
|            47 | DQ12     | Data line                     |             48 | DQ44     | Data line             |
|            49 | DQ13     | Data line                     |             50 | DQ45     | Data line             |
|            51 | DQ14     | Data line                     |             52 | DQ46     | Data line             |
|            53 | DQ15     | Data line                     |             54 | DQ47     | Data line             |
|            55 | Vss      | Ground                        |             56 | Vss      | Ground                |
|            57 | NC       | No connection                 |             58 | NC       | No connection         |
|            59 | NC       | No connection                 |             60 | NC       | No connection         |
|            61 | CLK0     | Clock                         |             62 | CKE0     | Clock enable          |
|            63 | Vdd      | Power supply                  |             64 | Vdd      | Power supply          |
|            65 | RAS#     | Row address strobe            |             66 | CAS#     | Column address strobe |
|            67 | WE#      | Write enable                  |             68 | CKE1     | Clock enable          |
|            69 | CS0#     | Chip select                   |             70 | A12/NC   | Address line          |
|            71 | CS1#     | Chip select                   |             72 | A13/NC   | Address line          |
|            73 | NC       | No connection                 |             74 | CLK1     | Clock                 |
|            75 | Vss      | Ground                        |             76 | Vss      | Ground                |
|            77 | NC       | No connection                 |             78 | NC       | No connection         |
|            79 | NC       | No connection                 |             80 | NC       | No connection         |
|            81 | Vdd      | Power supply                  |             82 | Vdd      | Power supply          |
|            83 | DQ16     | Data line                     |             84 | DQ48     | Data line             |
|            85 | DQ17     | Data line                     |             86 | DQ49     | Data line             |
|            87 | DQ18     | Data line                     |             88 | DQ50     | Data line             |
|            89 | DQ19     | Data line                     |             90 | DQ51     | Data line             |
|            91 | Vss      | Ground                        |             92 | Vss      | Ground                |
|            93 | DQ20     | Data line                     |             94 | DQ52     | Data line             |
|            95 | DQ21     | Data line                     |             96 | DQ53     | Data line             |
|            97 | DQ22     | Data line                     |             98 | DQ54     | Data line             |
|            99 | DQ23     | Data line                     |            100 | DQ55     | Data line             |
|           101 | Vdd      | Power supply                  |            102 | Vdd      | Power supply          |
|           103 | A6       | Address line                  |            104 | A7       | Address line          |
|           105 | A8       | Address line                  |            106 | BA0      | Bank address          |
|           107 | Vss      | Ground                        |            108 | Vss      | Ground                |
|           109 | A9       | Address line                  |            110 | BA1      | Bank address          |
|           111 | A10/AP   | Address line / Auto precharge |            112 | A11      | Address line          |
|           113 | Vdd      | Power supply                  |            114 | Vdd      | Power supply          |
|           115 | DQM2     | Data mask                     |            116 | DQM6     | Data mask             |
|           117 | DQM3     | Data mask                     |            118 | DQM7     | Data mask             |
|           119 | Vss      | Ground                        |            120 | Vss      | Ground                |
|           121 | DQ24     | Data line                     |            122 | DQ56     | Data line             |
|           123 | DQ25     | Data line                     |            124 | DQ57     | Data line             |
|           125 | DQ26     | Data line                     |            126 | DQ58     | Data line             |
|           127 | DQ27     | Data line                     |            128 | DQ59     | Data line             |
|           129 | Vdd      | Power supply                  |            130 | Vdd      | Power supply          |
|           131 | DQ28     | Data line                     |            132 | DQ60     | Data line             |
|           133 | DQ29     | Data line                     |            134 | DQ61     | Data line             |
|           135 | DQ30     | Data line                     |            136 | DQ62     | Data line             |
|           137 | DQ31     | Data line                     |            138 | DQ63     | Data line             |
|           139 | Vss      | Ground                        |            140 | Vss      | Ground                |
|           141 | SDA      | Serial data line              |            142 | SCL      | Serial clock line     |
|           143 | Vdd      | Power supply                  |            144 | Vdd      | Power supply          |

| Pin Front | Pin Back | Description                       |
| --------- | -------- | --------------------------------- |
| 1         | Vss      | Ground (0V)                       |
| 2         | Vss      | Ground (0V)                       |
| 3         | DQ0      | Data Input/Output 0               |
| 4         | DQ32     | Data Input/Output 32              |
| 5         | DQ1      | Data Input/Output 1               |
| 6         | DQ33     | Data Input/Output 33              |
| 7         | DQ2      | Data Input/Output 2               |
| 8         | DQ34     | Data Input/Output 34              |
| 9         | DQ3      | Data Input/Output 3               |
| 10        | DQ35     | Data Input/Output 35              |
| 11        | Vdd      | Power Supply Voltage (3.3V)       |
| 12        | Vdd      | Power Supply Voltage (3.3V)       |
| 13        | DQ4      | Data Input/Output 4               |
| 14        | DQ36     | Data Input/Output 36              |
| 15        | DQ5      | Data Input/Output 5               |
| 16        | DQ37     | Data Input/Output 37              |
| 17        | DQ6      | Data Input/Output 6               |
| 18        | DQ38     | Data Input/Output 38              |
| 19        | DQ7      | Data Input/Output 7               |
| 20        | DQ39     | Data Input/Output 39              |
| 21        | Vss      | Ground (0V)                       |
| 22        | Vss      | Ground (0V)                       |
| 23        | DQM0     | Data Mask 0 (for Data Bits 0-7)   |
| 24        | DQM4     | Data Mask 4 (for Data Bits 32-39) |
| 25        | DQM1     | Data Mask 1 (for Data Bits 8-15)  |
| 26        | DQM5     | Data Mask 5 (for Data Bits 40-47) |
| 27        | Vdd      | Power Supply Voltage (3.3V)       |
| 28        | Vdd      | Power Supply Voltage (3.3V)       |
| 29        | A0       | Address Bit 0                     |
| 30        | A3       | Address Bit 3                     |
| 31        | A1       | Address Bit 1                     |
| 32        | A4       | Address Bit 4                     |
| 33        | A2       | Address Bit 2                     |
| 34        | A5       | Address Bit 5                     |
| 35        | Vss      | Ground (0V)                       |
| 36        | Vss      | Ground (0V)                       |
| 37        | DQ8      | Data Input/Output 8               |
| 38        | DQ40     | Data Input/Output 40              |
| 39        | DQ9      | Data Input/Output 9               |
| 40        | DQ41     | Data Input/Output 41              |
| 41        | DQ10     | Data Input/Output 10              |
| 42        | DQ42     | Data Input/Output 42              |
| 43        | DQ11     | Data Input/Output 11              |
| 44        | DQ43     | Data Input/Output 43              |
| 45        | Vdd      | Power Supply Voltage (3.3V)       |
| 46        | Vdd      | Power Supply Voltage (3.3V)       |
| 47        | DQ12     | Data Input/Output 12              |
| 48        | DQ44     | Data Input/Output 44              |
| 49        | DQ13     | Data Input/Output 13              |
| 50        | DQ45     | Data Input/Output 45              |
| 51        | DQ14     | Data Input/Output 14              |
| 52        | DQ46     | Data Input/Output 46              |
| 53        | DQ15     | Data Input/Output 15              |
| 54        | DQ47     | Data Input/Output 47              |
| 55        | Vss      | Ground (0V)                       |
| 56        | Vss      | Ground (0V)                       |
| 57        | NC       | No Connection                     |
| 58        | NC       | No Connection                     |
| 59        | NC       | No Connection                     |
| 60        | NC       | No Connection                     |
| 61        | CLK0     | Clock Signal 0                    |
| 62        | CKE0     | Clock Enable Signal 0             |
| 63        | Vdd      | Power Supply Voltage (3.3V)       |
| 64        | Vdd      | Power Supply Voltage (3.3V)       |
| 65        | RAS#     | Row Address Strobe                |
| 66        | CAS#     | Column Address Strobe             |
| 67        | WE#      | Write Enable                      |
| 68        | CKE1     | Clock Enable Signal 1             |
| 69        | CS0#     | Chip Select 0                     |
| 70        | A12/NC   | Address Bit 12 or No Connection   |
| 71        | CS1#     | Chip Select 1                     |
| 72        | A13/NC   | Address Bit 13 or No Connection   |
| 73        | NC       | No Connection                     |
| 74        | CLK1     | Clock Signal 1                    |
| 75        | Vss      | Ground (0V)                       |
| 76        | Vss      | Ground (0V)                       |
| 77        | NC       | No Connection                     |
| 78        | NC       | No Connection                     |
| 79        | NC       | No Connection                     |
| 80        | NC       | No Connection                     |
| 81        | Vdd      | Power Supply Voltage (3.3V)       |
| 82        | Vdd      | Power Supply Voltage (3.3V)       |
| 83        | DQ16     | Data Input/Output 16              |
| 84        | DQ48     | Data Input/Output 48              |
| 85        | DQ17     | Data Input/Output 17              |
| 86        | DQ49     | Data Input/Output 49              |
| 87        | DQ18     | Data Input/Output 18              |
| 88        | DQ50     | Data Input/Output 50             |
| 89        | DQ19     | Data Input/Output 19             |
| 90        | DQ51     | Data Input/Output 51             |
| 91        | Vss      | Ground (0V)                     |
| 92        | Vss      | Ground (0V)                     |
| 93        | DQ20     | Data Input/Output 20             |
| 94        | DQ52     | Data Input/Output 52             |
| 95        | DQ21     | Data Input/Output 21             |
| 96        | DQ53     | Data Input/Output 53             |
| 97        | DQ22     | Data Input/Output 22             |
| 98        | DQ54     | Data Input/Output 54             |
| 99        | DQ23     | Data Input/Output 23             |
| 100       | DQ55     | Data Input/Output 55             |
| 101       | Vdd      | Power Supply Voltage (3.3V)      |
| 102       | Vdd      | Power Supply Voltage (3.3V)      |
| 103       | A6       | Address Bit 6                   |
| 104       | A7       | Address Bit 7                   |
| 105       | A8       | Address Bit 8                   |
| 106       | BA0      | Bank Address Bit 0              |
| 107       | Vss      | Ground (0V)                     |
| 108       | Vss      | Ground (0V)                     |
| 109       | A9       | Address Bit 9                   |
| 110       | BA1      | Bank Address Bit 1              |
| 111       | A10/AP   | Address Bit 10 or Address Parity |
| 112       | A11      | Address Bit 11                   |
| 113       | Vdd      | Power Supply Voltage (3.3V)      |
| 114       | Vdd      | Power Supply Voltage (3.3V)      |
| 115       | DQM2     | Data Mask 2 (for Data Bits 16-23)|
| 116       | DQM6     | Data Mask 6 (for Data Bits 48-55)|
| 117       | DQM3     | Data Mask 3 (for Data Bits 24-31)|
| 118       | DQM7     | Data Mask 7 (for Data Bits 56-63)|
| 119       | Vss      | Ground (0V)                     |
| 120       | Vss      | Ground (0V)                     |
| 121       | DQ24     | Data Input/Output 24             |
| 122       | DQ56     | Data Input/Output 56             |
| 123       | DQ25     | Data Input/Output 25             |
| 124       | DQ57     | Data Input/Output 57             |
| 125       | DQ26     | Data Input/Output 26             |
| 126       | DQ58     | Data Input/Output 58             |
| 127       | DQ27     | Data Input/Output 27             |
| 128       | DQ59     | Data Input/Output 59             |
| 129       | Vdd      | Power Supply Voltage (3.3V)      |
| 130       | Vdd      | Power Supply Voltage (3.3V)      |
| 131       | DQ28     | Data Input/Output 28             |
| 132       | DQ60     | Data Input/Output 60             |
| 133       | DQ29     | Data Input/Output 29             |
| 134       | DQ61     | Data Input/Output 61             |
| 135       | DQ30     | Data Input/Output 30             |
| 136       | DQ62     | Data Input/Output 62             |
| 137       | DQ31     | Data Input/Output 31             |
| 138       | DQ63     | Data Input/Output 63             |
| 139       | Vss      | Ground (0V)                     |
| 140       | Vss      | Ground (0V)                     |
| 141       | SDA      | I2C Serial Data                  |
| 142       | SCL      | I2C Serial Clock                 |
| 143       | Vdd      | Power Supply Voltage (3.3V)      |
| 144       | Vdd      | Power Supply Voltage (3.3V)      |

## 二、使用

-   TODO（成功打样并工作后更新）
