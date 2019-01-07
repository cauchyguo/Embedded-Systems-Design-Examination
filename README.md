###Embedded-Systems-Design-Examination
嵌入式系统考试，背就完事！
+ 嵌入式系统与桌面通用系统的区别
+ **嵌入式系统与桌面通用系统的区别**

嵌入式处理器的基本特征**

嵌入式处理器的种类及特点（MCU、 、DSP、 、MPU、 、
SOC ）**

典型嵌入式处理器的特点及应用场景（ARM、 、
MIPS 、POWERPC ）**

嵌入式软件系统的体系结构及各个层次的任务**

嵌入式操作系统的主要特性**

+ **NOR型闪存的特点**
    - 具有独立的地址线、数据线，支持快速随机访问，容量
较小；
    - 具有芯片内执行（XIP， eXecute In Place）的功能，按
照字节为单位进行随机写；
    - NOR型闪存适合用来存储少量的可执行代码。

+ **NAND型闪存的特点**
    - 地址线、数据线共用，单元尺寸比NOR型器件小，具有
更高的价格容量比，可以达到高存储密度和大容量；
    - 读、写操作单位采用512字节的页面；
    - NAND更适合作为高密度数据存储

+ **NAND闪存管理中的问题**
    - Flash的写入操作只能把对应位置的1修改为0，而不能把0修改为
1(擦除Flash就是把对应存储块的内容恢复为1)，因此，一般情况下，向
Flash写入内容时，需要先擦除对应的存储区间，这种擦除是以块(block)
为单位进行的。
    - 损耗均衡(Wear Leveling)：闪存上的每个块都具有擦除次数的上限，
被称为擦除周期计数(erase cycle count)。
    - 坏块处理问题： NAND器件中的坏块是随机分布的，由于消除坏块
的代价太高，因而使用NAND器件的初始化阶段进行扫描以发现坏块，
并将坏块标记为不可用(非0xFF)。
    - 掉电保护问题：文件系统应能保证在系统突然断电时，最大限度地
保护数据，使文件恢复到掉电前的一个一致性状态。
    - 等等。。。。
    - 传统的文件系统如ext2、FAT等，用作Flash的文件系统会有诸多弊端

+ **根文件系统作用**
    - 根文件系统首先是内核启动时所mount的第一
个文件系统， 内核代码映像文件保存在根文件系统
中，而系统引导启动程序会在根文件系统挂载之后
从中把一些基本的初始化脚本和服务等加载到内存
中去运行。

由于设备驱动错误，导致操作系统崩溃约占30-40%

+ **外部设备与CPU的通讯信息，主要包括**
    - 控制信息：告诉要进行什么处理
    - 状态信息：当前设备的状态
    - 数据信息：不同的设备，传输数据类型及编码各异。

+ **输入、输出方式控制**
    - 直接控制I/O方式：通过指令直接对端口进行输入、输出
控制。如x86的in、out指令。
    - 内存映射方式：可以访问较大的地址空间，实现快速数据
交换，如：ISA总线可以映射的空间为0xC8000～0xEFFF。
    - 中断方式：采用中断实现数据的输入/输出。
    - DMA方式： 采用DMA控制器，实现数据传输。
<数据量不大的情况下，如字符设备，常采用中断方式；
大量数据传输的I/O设备，如磁盘、网卡等设备，常采
用DMA方式，以减少CPU资源占用。>

+ **驱动程序与应用程序的区别**
    - 主动与被动的区别。应用程序有一个main函
数，总是从些函数开始主动执行一个任务，
而驱动程序安装之后，便停止工作，并等待
被应用程序调用。
    - 使用的库函数不同。
    - 程序运行的区域不同。驱动程序工作在内核
态；应用程序工作在用户态

+ **设备文件和设备号**
    - 主设备号，标识设备的种类，使用的驱动程序
    - 次设备号，标识使用同一设备驱动程序的不同硬件设备