# 故障诊断多模态数据集推荐

## HUST电机多模态数据集

1. **电机故障测试是使用Spectra-Quest机械故障模拟器进行的，如下图所示。** 

![F4](E:\迅雷下载\F4.png)

2. **原始数据文件包含24个文件（6种健康状态；4种工作条件），每个文件均为txt格式。 例如，文件名“H_5HZ”表示在5Hz工作条件下的健康电机。 健康状态由以下代码表示，处于六种健康状态的电机包括：** 

- 健康状态——H
- 轴承故障——BF
- 转子弯曲——BOW
- 转子断条——BROKEN
- 转子不对中——MISAL
- 电压不平衡——UNBAL 

3. **需要注意的是，所有故障都是人为预设的。 运行条件实验中设置了4种不同的运行条件。运行条件包括：**

 5Hz、10Hz、20Hz、30Hz

4. **采样设置** 

采样频率设置为25.6kHz。每次采样记录共163840个数据点（即6.4s）。

5. **版权声明**

   - 这些数据集是公开可用的，任何人都可以利用它们来验证各种诊断算法的有效性。

   - 凡是使用HUSTmotor多模态数据集进行研究的出版物，都请引用以下论文作为参考文献。

   **Chao Zhao, Weiming Shen, Enrico Zio, Hui Ma, Multimodal unified generalization and translation network for intelligent fault diagnosis under dynamic environments. Engineering Applications of Artificial Intelligence, Volume 162, Part C, 2025, 112559.**

6. **下载地址**

   - Data of Google Drive: https://drive.google.com/drive/folders/1XmahwIQ4o66FC3dpOaeTV-gqz2dd0XBw?usp=sharing

   - Data of Quark Netdisk: https://pan.quark.cn/s/61c75de606e8



## 韩国科学技术院多模态数据集

1. **旋转机械试验台由三相感应电机、扭矩计、齿轮箱、轴承座A、轴承座B、转子和磁滞制动器组成。**

   ![img](https://ars.els-cdn.com/content/image/1-s2.0-S2352340923001671-gr5.jpg)

2. **文件名解读** 

   - 振动文件格式说明：**0Nm_BPFI_03.mat**：该文件包含在0 Nm 载荷条件下，轴承两个机壳在 x 和 y 方向的振动数据，其中内圈存在0.3 mm 缺陷。
   - 声音文件格式说明：**0Nm_BPFI_03.mat**：该文件包含在0Nm负载条件下具有0.3毫米内圈故障的轴承的声学数据。
   - 温度和电流文件格式说明：**0Nm_BPFI_03.tdms**：该文件包含温度数据以及轴承三相电流数据，在0 Nm负载条件下，内圈存在0.3 mm故障。
   - 变转速振动文件格式说明：**vibration_inner_0.csv ∼ vibration_inner_6.csv**：每个文件均包含两个轴承座在变速条件下的x和y方向振动数据，时长300秒。内部有缺陷的轴承安装在轴承座B中。
   - 变转速电流文件格式说明：**current_inner_0.csv ∼ current_inner_6.csv**：每份文件包含在不同速度条件下主电机的R相、S相和T相电流数据的300秒长度。在轴承座B中安装了具有内部故障的轴承。
   - 旋转速度变换文件说明：**rpm_normal_0.csv∼rpm_normal_6.csv** ：每个文件包含主电机在变速条件下的转速变化300秒的记录。

3. **需要注意的是，所有故障都是人为预设的。 运行条件实验中设置了几种不同的运行条件。运行条件包括：**

   - 恒定转速


| 数据类型         | 故障位置 | 故障类型 | 故障严重程度 | 时长（秒） | 负载（Nm） | 转速（RPM） | 采样率（kHz） |
| ---------------- | -------- | -------- | ------------ | ---------- | ---------- | ----------- | ------------- |
| 振动、温度、电流 | -        | 正常     | -            | 120        | 0、2、4    | 3010        | 25.6          |
|                  | 磁盘4    | 不平衡   | 583 mg       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 1169 mg      | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 1751 mg      | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 2239 mg      | 60         | 0、2、4    | 3010        | 25.6          |
|                  | 轴承座A  | 不对中   | 0.318 mm     | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          | 内圈故障 | 0.3 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 0.5 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 0.3 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 1.0 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          | 外圈故障 | 0.3 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 1.0 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 0.3 mm       | 60         | 0、2、4    | 3010        | 25.6          |
|                  |          |          | 1.0 mm       | 60         | 0、2、4    | 3010        | 25.6          |
| 声学             | -        | 正常     | -            | 60         | 0          | 3010        | 51.2          |
|                  | 轴承座A  | 内圈故障 | 0.3 mm       | 60         | 0          | 3010        | 51.2          |
|                  |          |          | 1.0 mm       | 60         | 0          | 3010        | 51.2          |
|                  |          | 外圈故障 | 0.3 mm       | 60         | 0          | 3010        | 51.2          |
|                  |          |          | 1.0 mm       | 60         | 0          | 3010        | 51.2          |

- 变转速

  | 数据类型     | 转速工况 | 故障位置   | 故障类型 | 时长（秒）/（每个文件） | 负载（Nm） | 转速（RPM）| 采样率（kHz） |
|--------------|----------|------------|----------|------------------------|------------|------------|---------------|
| 振动         | 恒定     | 轴承座A    | 正常     | 600                    | 0          | 3010       | 25.6          |
|              |          |            | 内圈故障 | 600                    | 0          | 3010       | 25.6          |
|              |          |            | 外圈故障 | 600                    | 0          | 3010       | 25.6          |
|              |          |            | 滚珠故障 | 600                    | 0          | 3010       | 25.6          |
|              | 变化     | 轴承座B    | 正常     | 2100（每个文件300）| 0          | 680～2460  | 25.6          |
|              |          |            | 内圈故障 | 2100（每个文件300）| 0          | 680～2460  | 25.6          |
|              |          |            | 外圈故障 | 2100（每个文件300）| 0          | 680～2460  | 25.6          |
|              |          |            | 滚珠故障 | 2100（每个文件300）| 0          | 680～2460  | 25.6          |
| 电机电流     | 变化     | 轴承座B    | 正常     | 2100（每个文件300）| 0          | 680～2460  | 100           |
|              |          |            | 内圈故障 | 2100（每个文件300）| 0          | 680～2460  | 100           |
|              |          |            | 外圈故障 | 2100（每个文件300）| 0          | 680～2460  | 100           |
|              |          |            | 滚珠故障 | 2100（每个文件300）| 0          | 680～2460  | 100           |

4. **采样频率**

   - 恒定转速下，振动、温度、电流的采样频率为25.6Hz
   - 恒定转速下，声音的采样频率为51.2Hz
   - 变转速下，振动采样频率为25.6Hz
   - 变转速下，电机电流的采样频率为100Hz

5. **版权声明：**

   韩国大田市韩国科学技术院机械工程系噪声与振动控制增强研究中心人类实验室已同意，这些数据集可作为本出版物的一部分公开发布。

   **Jung W, Kim S H, Yun S H, et al. Vibration, acoustic, temperature, and motor current dataset of rotating machine under varying operating conditions for fault diagnosis[J]. Data in brief, 2023, 48: 109049.**

6. **下载地址：**

   - [Vibration and Motor Current Dataset of Rolling Element Bearing Under Varying Speed Conditions for Fault Diagnosis: Subset1 (Original data)](https://data.mendeley.com/datasets/vxkj334rzv) (Mendeley Data).
   - [Vibration and Motor Current Dataset of Rolling Element Bearing Under Varying Speed Conditions for Fault Diagnosis: Subset2 (Original data)](https://data.mendeley.com/datasets/x3vhp8t6hg) (Mendeley Data).
   - [Vibration and Motor Current Dataset of Rolling Element Bearing Under Varying Speed Conditions for Fault Diagnosis: Subset3 (Original data)](https://data.mendeley.com/datasets/j8d8pfkvj2) (Mendeley Data).
   - [Vibration, Acoustic, Temperature, and Motor Current Dataset of Rotating Machine Under Varying Load Conditions for Fault Diagnosis (Original data)](https://data.mendeley.com/datasets/ztmf3m7h5x) (Mendeley Data).

## UM齿轮箱数据集

1. **测试台A由一个电机驱动，传动系统包含一个行星齿轮箱和一个平行齿轮箱，传动括行星齿轮箱中太阳轮G1，平行齿轮箱中第二级传动轴上齿轮G2和第二级传动轴的轴承B1。系统另一端为一个制动阻尼器。**

   ![test_rig_A](https://github.com/CH-0909/UM-Gearbox-Dataset/raw/main/images/test_rig_A.jpg)

2. **测试台B的传动系统包含了一个行星齿轮箱和三个平行齿轮箱。测试台B上采用的故障部件与测试台A相同（G2仅包含普通程度故障）。测试台B设置为无负载，转速设定为600，1200和1800转/分钟。**

   ![test_rig_B.jpg](https://github.com/CH-0909/UM-Gearbox-Dataset/raw/main/images/test_rig_B.jpg)

3. **运行条件和故障类型：**

   - 太阳轮G1包含破齿（CT），缺齿（MT）,齿根缺口（RC）和表面磨损（SF）四种故障。齿轮G2包含破齿（CT），缺齿（MT）,齿根缺口（RC）和表面磨损（SF）四种故障以及这四种故障的加重情况，即重度破齿（HCT），重度缺齿（HMT）,重度齿根缺口（HRC）和重度表面磨损（HSF）。轴承B1包含了三种故障，即内圈故障（IR），外圈故障（OR）和滚珠故障（B）。实验中电机输入转速设定为600，1200和1800r/分钟，制动阻尼（即负载）设定为0-4L。测试台A上的实验是对三个部件的故障试验，单一故障种类有180种，此外有多种混合故障类型，G1-G2混个故障有192种，G1-B1混合故障有72种，G2-B1混合故障有144种，G1-G2-B1混合故障有96种。测试台A上安装了2个加速度传感器。每个种类的数据采集时长大约为3600秒。
   - 测试台B上的实验采集单一故障36种；复合故障G1-B1，G1-G2，G2-B1各包含48种类型，共144种；复合故障G1-G2-B1包含36种类型。测试台B上安装了11种传感器，包括5个加速度传感器，2个电流传感器，1个麦克风，1个转矩传感器和2个自制传感器。其中每个种类的数据采集时长大约为900秒。

4. **采用频率**

   - 测试台A的采样频率为25.6Hz
   - 测试台B转矩传感器和自制传感器的采样频率为25.6kHz，其他传感器采样频率为51.2kHz。

5. **版权声明**

   该数据集目前已应用于相关研究，具体如下： 

   - **Chen, H., Li, C., Yang, W., Liu, J., An, X., & Zhao, Y. "Deep balanced cascade forest: An novel fault diagnosis method for data imbalance." ISA transactions, 126 (2022): 428-439.**
   - **H. Chen, X. -b. Wang and Z. -X. Yang, "Fast Robust Capsule Network With Dynamic Pruning and Multiscale Mutual Information Maximization for Compound-Fault Diagnosis," in IEEE/ASME Transactions on Mechatronics, vol. 28, no. 2, pp. 838-847, April 2023, doi: 10.1109/TMECH.2022.3214865.**
   - **Yang, Z. X., Li, C. S., Wang, X. B., & Chen, H.* (2022). “Intelligent fault monitoring and diagnosis of tunnel fans using a hierarchical cascade forest,” ISA transactions, doi: 10.1016/j.isatra.2022.10.037.**
   - **H. Chen, X. -B. Wang, J. -m. Li and Z. -X. Yang, "Dynamic Focusing Network for Semisupervised Mechanical Fault Diagnosis of Rotating Machinery," in IEEE Transactions on Industrial Informatics, vol. 20, no. 10, pp. 11575-11586, Oct. 2024, doi: 10.1109/TII.2024.3409443.**
   - **Chen, H., Wang, X. B., Yang, Z. X., & Li, J. M. (2024). Privacy-preserving intelligent fault diagnostics for wind turbine clusters using federated stacked capsule autoencoder. Expert Systems with Applications, 254, 124256.**

6. 下载地址

   测试台A数据集： https://pan.baidu.com/s/1SHAE6HzOd3mmMPHQcOD6zA?pwd=v3tt 密码：v3tt 

   测试台B数据集：  https://pan.baidu.com/s/1rOezeU2fnMv1p-mE-4qSWA?pwd=977k 密码: 977k

## CUMTB风电变桨轴承

1. **比例缩放的变距轴承机械平台由伺服电机和比例缩放的变距轴承组成，如图3所示。该轴承按照实际变距轴承1:6的比例缩小，确保了因故障影响的设备的一致性。电机通过行星减速器驱动轴承旋转，并通过特定控制系统调节其速度。健康轴承和具有各种故障的轴承的振动和声学数据依次采样收集。考虑到风场的随机性，实验的操作条件和载荷均源自领先风力发电机组制造商提供的实际工作环境，以确保实验数据的真实性和合理性。**

   ![image-20260111094810078](C:\Users\11952\AppData\Roaming\Typora\typora-user-images\image-20260111094810078.png)

2. **收集了风力发电机桨距轴承在三种负载和两种转速下的11种故障类型的振动和声学数据：**

   - 负载：Cond_1、Cond_2、Cond_3
   - 转速：1RPM、3RPM

3. **Cond_3\1rpm\Health\vibandacoustic\va(1).csv: 该文件包含了在Cond_1条件下、转速为1r/分钟时，健康状态下的轴承在x方向和y方向上的振动数据以及声学参数。**

   ![image-20260111094411619](C:\Users\11952\AppData\Roaming\Typora\typora-user-images\image-20260111094411619.png)

   在特定负载和转速下收集的振动和声学数据存储在“.csv”文件中。在每个采样时间，记录以下六个变量的“vib_y_direction_A”、“vib_x_direction_A”、“vib_y_direction_B”“vib_x_direction_B”和“声学”。

4. **故障类型：**

   - ITRC：内圈齿根裂纹
   - RBC：滚动体裂纹
   - IRC：内圈裂纹
   - IRW：内圈滚道磨损
   - IRS：内圈滚道剥落
   - ORC：外圈滚道裂纹
   - ORW：外圈滚道磨损
   - ORS：外圈滚道剥落
   - IORC：内圈和外圈滚道裂纹
   - IORW：内圈和外圈滚道磨损
   - IORS：内圈和外圈滚道剥落

5. **采样设置：**

   38.5Hz

6. **版权声明：**

   若使用数据请引用：**Guo Y, He J, Pu J, et al. Vibration and acoustic data of pitch bearing in wind turbines under time-varying load for fault diagnosis[J]. Data in Brief, 2025: 111876.**

7. 下载地址：
   https://data.mendeley.com/datasets/2n9jkd384k/1;
   https://data.mendeley.com/datasets/md6hnhpv3b/1

   

## 逆变器驱动永磁同步电机系统故障数据集

1. **实验装置由四个主要子系统组成：电力电子逆变器、永磁同步电机（PMSM）、控制系统以及数据采集系统，如图9所示。该装置设计用于在各种运行条件下进行全面的故障模拟和数据收集。**

   ![image-20260111115323856](C:\Users\11952\AppData\Roaming\Typora\typora-user-images\image-20260111115323856.png)

2. **采样频率**

   10Hz

3. **故障类型和特征参数：**

   包含电流，电压和温度数据。

   ![image-20260111121353614](C:\Users\11952\AppData\Roaming\Typora\typora-user-images\image-20260111121353614.png)

   | 类别 | 位置        | 故障描述       | 样本数量 |
   | :--- | :---------- | :------------- | :------- |
   | F0   | 无          | 正常运行工况   | 4295     |
   | F1   | S3          | 高端开路故障   | 692      |
   | F2   | S6          | 低端开路故障   | 1122     |
   | F3   | S2          | 低端短路故障   | 407      |
   | F4   | S2          | 高端短路故障   | 341      |
   | F5   | S5          | 高端短路故障   | 412      |
   | F6   | 半桥模块1   | 过热故障       | 854      |
   | F7   | 半桥模块1&2 | 过热故障       | 1735     |
   | F8   | 半桥模块3   | 过热故障       | 1034     |

| 特征参数 | 特征描述     | 传感器类型                | 数值范围  |
| :------- | :----------- | :------------------------ | :-------- |
| Ia       | A相进线电流  | ACS712 20A 电流传感器     | 0 - 1023  |
| Ib       | B相进线电流  | ACS712 20A 电流传感器     | 0 - 1023  |
| Vdc      | 直流母线电压 | ACS712 20A+100Ω分压电阻    | 0 - 1023  |
| Idc      | 直流母线电流 | ACS712 20A 电流传感器     | 0 - 1023  |
| T1       | 半桥1温度    | 10kΩ NTC 热敏电阻         | 0 - 1023  |
| T2       | 半桥2温度    | 10kΩ NTC 热敏电阻         | 0 - 1023  |
| T3       | 半桥3温度    | 10kΩ NTC 热敏电阻         | 0 - 1023  |
| Vd       | 驱动电压     | ACS712 20A+100Ω分压电阻    | 0 - 1023  |

4. **版权声明：**

   This dataset is released under Creative Commons Attribution 4.0 International License.

   **Bacha A, El Idrissi R, Idrissi K J, et al. Comprehensive dataset for fault detection and diagnosis in inverter-driven permanent magnet synchronous motor systems[J]. Data in Brief, 2025, 58: 111286.**

5. **下载地址**

   Data identification number: [10.5281/zenodo.14482932](https://doi.org/10.5281/zenodo.14482932)
   Direct URL to data: https://zenodo.org/records/14482932

## JUST 回转支承数据集

1. **如图 1 所示,展示了完整的回转支承故障试验 平台,其中包括回转支承、啮合小齿轮、回转支承底 座、换向箱、同步带、调速电机、调速器和负载装置等 各部件。 回转支承故障试验台的硬件均采用市面上 成熟稳定的通用型号。**

   ![image-20260111170947701](C:\Users\11952\AppData\Roaming\Typora\typora-user-images\image-20260111170947701.png)

2. **原始数据文件包含24个文件（4种健康状态；9种工作条件），每个 csv 文件一共包含 7 列数据,第 1、4、5、6 列 为竖直方向的振动信号,第 2、3 列为水平方向的振 动信号,第 7 列为声发射信号。 每个 csv 文件按采 集时间-故障类型-转速-倾覆力-每种工况采样次 数来进行先后命名, 如 “ 20221208-N-2rpm-0N-1 ”。** 

- 内外圈及滚子部件 均完好的健康回转支承,将其标记为 N;
- 内圈带有 约 1 mm 深裂纹凹孔的故障回转支承,将其标记为 I;
- 外圈带有约 1 mm 深不规则划痕的故障回转支 承,将其标记为 O;
- 一个滚子磨损的滚动体故障回 转支承,将其标记为 B1。

3. **需要注意的是，所有故障都是人为预设的。 运行条件实验中设置了不同的运行条件。运行条件包括：**

- 输出转速为2、6、12r/min
- 倾覆力0、30、60N

4. **采样设置** 

采样频率设置为50kHz。

5. **版权声明**：

   **周宏根,任小蝶,孙丽,等.JUST回转支承故障试验数据分析[J].兵工学报,2024,45(10):3744-3753.**

6. **下载地址**

   - https://data.mendeley.com/datasets/hwg8v5j8t6/1

   - https://data.mendeley.com/datasets/rcxgmdxhbr/1
