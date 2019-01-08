## 嵌入式系统考试  
#### 背就完事！ 

+ **嵌入式系统定义** 
    - IEEE定义:嵌入式系统是“控制、监视或者辅助设备、机器和车间运行的装置
    - 普遍接受的定义:嵌入式系统是以应用为中心，以计算机技术为基础，采用可剪裁软硬件，适用于对功能、可靠性、成本、体积、功耗等有严格要求的专用计算机系统。
    
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

+ **嵌入式软件系统的体系结构**   
![嵌入式软件系统的体系结构图](https://github.com/cauchyguo/Embedded-Systems-Design-Examination/blob/master/img/soft_art.png "Linux程序开发流程图")


+ **ARM 微处理器的特点**  
    - 高性能、低能耗、低功耗  
    - 大量的寄存器，都可用于多种用途  
    - Load/Store体系结构，非常强大的多寄存器Load和Store指令  
    - 3地址指令(两个源操作数寄存器和结果寄存器独立设定)
    - 每条指令都条件执行，包含能在单时钟周期执行的单挑指令内完成一项普通的移位操作和一项普通的ALU操作
    - 能过协处理器指令集来拓展ARM指令集，包括在编程模式下增加了新的寄存器和数据类型
    - 在Thumb体系结构中以高密度16位压缩形式来表示指令集

+ **CISC与RISC体系结构的特点及区别**
    - CISC结构微处理器的特点
        - 数据传输指令： MOV AX， [DI+1000]
        - 机器码长度为4字节，指令执行时间为17个时钟周期。
        - 除法指令： DIV BX
        - 机器码长度为2字节，指令执行时间为155个时钟周期。
    - RISC体系结构处理器的特点
        - 指令具有相同的机器码位长。常见的为32位。对有些不足32
        位的指令都将无用位填0。
        - 95%的指令执行时间为一个时钟周期。剩余的5%指令也只需2
        个时钟周期。
        - 没有采用CISC实现复杂指令必用的微指令（微码）结构。节
        省了大量晶体管，但无法实现高性能指令。
        - 采用载入/存储(Load/Store)模式， 无法实现单指令存储器—存
        储器读写功能(存储器访问只能采用Load/Store指令)
    - 区别  
------------------
 | 指标 | RISC | CISC |  
 |:----------:|:-----------|:-----------|   
 | 指令集 | 一个周期执行一条指令，通过简单指令的组合实理复杂操作；指令长度固定。|指令长度不固定，执行需要多个周期。|
 | 流水线 | 流水线每周期前进一步。 | 指令的执行需要调用微代码的一个微程序。 |
 | 寄存器 | 更多通用寄存器。 | 用于特定目的的专用寄存器。 |
 | Load/Store结构 | 独立的Load和Store指令完成数据在寄存器和外部存储器之间的传输。 | 处理器能够直接处理存储器中的数据。 |  

+ ~~**冯. 诺依曼结构和哈佛结构的特点及区别**~~

+ **ARM处理器的 7 种工作模式** :point_left:
![ARM处理器的7种模式](https://github.com/cauchyguo/Embedded-Systems-Design-Examination/blob/master/img/work_mode.png "ARM处理器的7种模式图片")


+ **ALinux 发展的 5 大支柱** :point_left:
    - Unix操作系统
    - Minix操作系统
    - GNU计划
    - POSIX标准
    - Internet
    
+ **中断处理过程** :point_left:
    - 硬件部分
        1. 复制CPSR到SPSR_<mode>
        2. 设置正确的CPSR位
        3. 切换到<mode>
        4. 保存返回地址到LR_<mode>
        5. 设置PC跳转到相应的异常向量表入口
    - 软件部分
        1. 把SPSR和LR压栈
        2. 把中断服务程序的寄存器压栈
        3. 开中断，允许嵌套中断
        4. 中断服务程序执行完后，恢复寄存器
        5. 弹出SPSR和PC，恢复执行
    
+ **Linux程序开发过程** :point_left:  
![Linux程序开发流程图](https://github.com/cauchyguo/Embedded-Systems-Design-Examination/blob/master/img/Linux_LCT.png "Linux程序开发流程图")

+ **嵌入式系统启动流程** :point_left: 
    - 硬件加电
    - 引导加载程序
        - Boot代码、Bootloader等
    - 操作系统内核，如Linux 内核
        - 根据特定的目标嵌入式硬件系统，定制的内核及启动参数
    - 加载文件系统
        - 包括根文件系统以及建立于Flash内存设备上的文件系统
    - 运行用户程序
        - 用户编写的完成特定功能的程序
        - 一些用户程序运行在一个嵌入式图形用户界面（GUI）上，常用
    的嵌入式GUI包括：MicroWindows 和MiniGuI等

+ **Boot Loader 的 stage1 与 stage2 主要步骤** :point_left: 
    - Boot Loader 的 stage1 
        - 硬件设备初始化、为加载 Boot Loader 的 stage2 准备 RAM 空间、拷贝 Boot Loader 的 stage2 到 RAM 空间中、设置好堆栈、跳转到 stage2 的 C 入口点
    - Boot Loader 的 stage2  
        - 初始化本阶段要使用到的硬件设备、检测系统内存映射(memory map)、将 kernel 映像和根文件系统映像从 flash 上读到RAM 空间中、为内核设置启动参数、调用内核

+ ~~**ARM-Linux 模块机制** :point_left:~~

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

+ 驱动代码
### ARM汇编实现20的阶乘  
--------------  
```
//BEQ：数据跳转指令，标志寄存器中Z标志位等于0时跳转到BEQ后面的标签处。
.global _start
.text
_start:
Mov R8, #20 @低32位初始化为20
Mov R9,#0 @高32位初始化为0
Sub R0,R8,#1 @初始化计数器
Loop：
MOV R1,R9 @暂存高位值
UMULL R8,R9,R0,R8 @[R9:R8]=R0*R8 @结果的低32位存于R8，高32位存于R9
MLA R9,R1,R0,R9 @R9=R1*R0+R9
SUBS R0，R0，#1 @计数器递减
BNE Loop @计数器不为0时继续循环
.Stop:
B Stop
.end @文件结束
```
### ARM汇编实现四个字位单位的复制(R0 to R1)，不足4字则以字位单位复制
```
.global _start
.equ NUM,18
.text  
.arm  
_start:  
        LDR     R0,  = SRC
        LDR     R1,  = DST
        MOV     R2,  # NUM
        MOV     SP,  # 0X9000 @SP为栈顶指针
        MOVS    R3, R2, LSR #2 @获得块拷贝(COPY_4WORD)次数
        BEQ     COPY_WORDS
        STMFD   SP!, {R5 - R8} @将R5 - R8压入栈堆(保护现场)
COPY_4WORD:
        LDMIA   R0!, {R5 - R8}
        STMIA   R1!, {R5 - R8}
        SUBS    R3, R3, #1
        BEQ     COPY_4WORD
        LDMFD   SP!, {R5 - R8}
COPY_WORDS:
        ANDS    R2, R2 #3 @按位与运算，得到COPY_WORD的迭代次数
        BEQ     STOP
COPY_WORD:
        LDR     R3, [R0], #4
        STR     R3, [R1], #4
        SUBS    R2, R2, #1
        BEQ     COPY_WORD
STOP:
        B       STOP
.ltorg
SRC:
    .long 1,2,3,4,5,6,7,8,9,0xa,0xb,0xc,0xd,0xe,0xf,0x10,0x11,0x12  
DST:
    .long 0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0
.end
```
-------------- 
@[cauchyguo](https://github.com/cauchyguo/) :+1:郭老师:ox::beer:
