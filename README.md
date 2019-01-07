## 嵌入式系统考试  
#### 背就完事！  
+ **嵌入式系统与桌面通用系统的区别** :point_left:
    - 嵌入式系统中运行的任务是专用而确定的：形式多样、面向
特定应用
    - 嵌入式系统处理器和处理器体系结构类型多
    - 嵌入式系统往往对实时性提出较高的要求，使用的操作系统一般是实时操作系统
    - 嵌入式系统运行需要高可靠性保障，比桌面系统
的故障容忍能力弱很多
    - 嵌入式系统大都有功耗约束(降低功耗，节省能量。)
    - 嵌入式系统比桌面通用系统可用资源少得多
    - 嵌入式系统的开发需要专用工具和特殊方法
        * 开发：交叉编译、交叉链接
        * 调试：仿真器、虚拟机
        * 更新：在线升级等
    - 嵌入式系统开发是一项综合的计算机应用技术
+ **嵌入式处理器的基本特征**
    - 控制单元：主要负责取指、译码和取操作数等基
本功能，并发送主要的控制指令。
        - 程序计数器PC：记录下一条程序指令的位置
        - 指令寄存器IR：存放所取的指令
    - 算术逻辑单元：算术运算单元，进行数学运算，
如加、减、除或数值的比较；另一部分是逻辑运算
单元，主要处理逻辑运算工作，如AND、OR、XOR或NOT等运算。
    - 寄存器：用于存储暂时性的数据。  
+ **相对通用处理器，嵌入式处理器有以下特点**
    - 体积小、集成度高、价格较低，这一特性与嵌入式系统的有限空间约束和较低的成本
架构需求相适应
    - 可扩展的处理器结构，能迅速开发出满足各种应用的高性能嵌入式系统
    - 功耗低，尤其是用于便携的无线及移动的计算和通信设备中靠
电池供电的嵌入式系统时，要求嵌入式处理器的功耗只有mw甚至um级
+ ~~**嵌入式处理器的种类及特点（MCU、 DSP、 MPU、 SOC ）**~~

+ ~~**典型嵌入式处理器的特点及应用场景（ARM、 MIPS 、POWERPC ）**~~

+ ~~**嵌入式软件系统的体系结构及各个层次的任务**~~

+ ~~**嵌入式操作系统的主要特性**~~

+ **典型嵌入式操作系统的特点及应用场景（Linux、VXwork、QNX、uC/OS）**:point_left:  

 | **操作系统** | **特点** | **应用场景** |
 |:----------:|:-----------|:-----------|
 | *Linux* |<li >广泛的硬件支持</li><li>内核高效稳定</li><li >开放源码，软件丰富</li><li >优秀的开发工具</li><li> 完善的网络通信和文件管理机制</li>|Android （面向智能手机及手持设备的嵌入式操作系统），女娲|
 | *VXwork* |<li >高可靠性</li><li>高实时性</li><li >可裁剪性好</li><li >非常昂贵</li>|用于美国“极地登陆者”号、 “深空二号” 和火星气候轨道器等登陆火星探测器|  
 | *QNX* |<li >高可靠性</li><li>高安全性</li><li >开放源码，软件丰富</li><li >优秀的开发工具</li><li> 完善的网络通信和文件管理机制</li>|广泛地嵌入到汽车、智能机器、智能仪器仪表、机顶盒、通讯设备、 PDA、黑莓操作系统等应用中|  
 | *uC/OS* |<li >开源、结构小、可剥夺、实时的</li><li>不支持时间片轮转调度法,并非“并发多道程序”</li><li >系统可靠性不保障</li><li >对图形应用的支持较弱| 主要应用于控制类等地段应用中，如:照相机行业、医 疗检测仪器、音响设施 |  

+ **ARM 微处理器的特点**  
    - 高性能、低能耗、低功耗  
    - 大量的寄存器，都可用于多种用途  
    - Load/Store体系结构，非常强大的多寄存器Load和Store指令  
    - 3地址指令(两个源操作数寄存器和结果寄存器独立设定)
    - 每条指令都条件执行，包含能在单时钟周期执行的单挑指令内完成一项普通的移位操作和一项普通的ALU操作
    - 能过协处理器指令集来拓展ARM指令集，包括在编程模式下增加了新的寄存器和数据类型
    - 在Thumb体系结构中以高密度16位压缩形式来表示指令集

+ **NOR型闪存的特点** :point_left:
    - 具有独立的地址线、数据线，支持快速随机访问，容量
较小；
    - 具有芯片内执行（XIP， eXecute In Place）的功能，按
照字节为单位进行随机写；
    - NOR型闪存适合用来存储少量的可执行代码。

+ **NAND型闪存的特点** :point_left:
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
    - 传统的文件系统如ext2、FAT等，用作Flash的文件系统会有诸多弊端

+ **根文件系统作用**
    - 根文件系统首先是内核启动时所mount的第一
个文件系统， 内核代码映像文件保存在根文件系统
中，而系统引导启动程序会在根文件系统挂载之后
从中把一些基本的初始化脚本和服务等加载到内存
中去运行。

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

+ **驱动程序与应用程序的区别** :point_left:
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
    
@[cauchyguo](https://github.com/cauchyguo/) :+1:郭老师:ox::beer:
