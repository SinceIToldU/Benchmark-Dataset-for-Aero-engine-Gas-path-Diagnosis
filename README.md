# Benchmark-Dataset-for-Aero-engine-Gas-path-Diagnosis
The Data Set Used in "Uncertainties in gas-path diagnosis of gas turbines: Representation and impact analysis".
(Tips: There is a Chinese version below)

==Context Help==

The data set includes two engine individuals of the same type, and there are manufacturing-induced differences between them.

"Decay_EngineB" is the "EngineB" after performance deterioration. The degree of performance deterioration is manifested by the rise in LPT outlet total temperature, with an increase of approximately 20K.

The three engine folders are divided into different sub folders according to the flight trajectory, with a total of 4:
flight trajectory for training, flight trajectory for testing, flight trajectory for fine-tuning1, flight trajectory for fine-tuning2

In different flight trajectory folders, they are divided into different sub folders again according to the type of  added sensor noise and bias, among which:
Noise0：Noise free
Noise1：White Gaussian noise
Noise2：Noise close to the actual situation（inherent bias+sinusoid disturbance+white Gaussian noise）
Noise3：Noise2+incremental drift

The data used for training and fine-tuning include operational data at -15℃, 0℃, 15℃ and 30℃ (sea surface temperature), while the data used for testing include operational data at TWO random sea surface temperatures between -15℃ and 30℃
The temperature of the training data is written on the name of the corresponding TXT file, and the temperature of  the test data is not visible.

There are 4 types of gas path components involved in the simulation: 
fan fault, compressor fault, high-pressure turbine fault, and low-pressure turbine fault.
Only ONE fault occurs in each flight and occurs before takeoff. The degree of the fault does not change during flight, and each component has the same fault degree in the above 3 engines.
The faulty component is written on the name of the corresponding TXT file.

==Data Index==
The Data in the TXT file are arranged in columns in the following order:
Run Time
Low Spool Speed 1
Low Spool Speed 2
High Spool Speed 1
High Spool Speed 2
Inlet Total Temperature
Inlet Total Pressure
Inlet Static pressure
Fan Outlet Total Temperature 1
Fan Outlet Total Temperature 2
Fan Outlet Total Pressure 1
Fan Outlet Total Pressure 2
Compressor Outlet Total Temperature 1
Compressor Outlet Total Temperature 2
Compressor Outlet Static Pressure 1
Compressor Outlet Static Pressure 2
Fuel Flow of Main Combustor
LPT Outlet Total Temperature 1
LPT Outlet Total Temperature 2
LPT Outlet Total Pressure 1
LPT Outlet Total Pressure 2
Fan External Outlet Total Temperature 1
Fan External Outlet Total Temperature 2
Nozzle Throat Area A8
Nozzle Outlet Area A9
Fan Variable Vane Angle
Compressor Variable Vane Angle

where, XX 1 is the measured value of the sensor, XX 2 is the output value of the airborne model, and other parameters without 1 or 2 are the measured value of the sensors

==Detailed Information==
For more details about the simulation, see
Uncertainties in Gas-path Diagnosis of Gas Turbines: Representation and Impact Analysis (As of Dec. 21, 2020,  )
Your comments and citation are welcome!


==内容说明==
数据包含两个同型号的发动机个体，个体间存在制造引起的性能差异

Decay_EngineB为发生性能衰退后的EngineB，衰退程度表现为相同输入条件下，涡轮后温度上升20℃，接近到期返厂大修时的一般衰退程度

三个发动机文件夹中又按飞行轨迹分为不同的文件夹，轨迹共4条：
训练用轨迹、测试用轨迹、微调用轨迹1、微调用轨迹2

在不同的飞行轨迹文件夹中，按传感器误差与噪声的类型又分为不同的文件夹，其中，
Noise0：无噪声
Noise1：高斯白噪声
Noise2：接近实际情况的噪声（固有偏差、周期扰动、白噪声）
Noise3：Noise2+允许的小范围漂移

用于训练和微调的数据包含了-15℃、0℃、15℃、30℃四个海平面温度下的数据，用于测试的数据包含了-15℃~30℃间随机的两个海平面温度下的数据
训练数据的对应温度写在相应的txt文件名称上，测试数据温度不可见

可能发生故障的气路部件共4种：风扇、压气机、高压涡轮、低压涡轮
每次飞行只发生一种故障，且在起飞前已发生，飞行中故障程度不发生变化，所有同类部件的故障程度相同
故障部件已写在相应的txt文件名称上

==数据索引==
txt中的数据按列顺序依次为
时间 
风扇转速1 
风扇转速2 
压气机转速1 
压气机转速2 
进气总温 
进气总压 
进气静压 
风扇出口总温1 
风扇出口总温2 
风扇出口总压1 
风扇出口总压2 
压气机出口总温1 
压气机出口总温2 
压气机出口静压1 
压气机出口静压2 
主燃油流量
低压涡轮出口总温1
低压涡轮出口总温2
低压涡轮出口总压1
低压涡轮出口总压2
风扇后外涵总压1
风扇后外涵总压2
风扇后外涵总温1
风扇后外涵总温2
喷口喉道面积A8
喷口排气面积A9
风扇导叶角度
压气机导叶角度

其中，xx1为传感器测量值，xx2为机载模型的输出值，其余不含1或2的为传感器测量值

==详细信息==
数据生成及不确定性模拟方法详见论文：
Uncertainties in Gas-path Diagnosis of Gas Turbines: Representation and Impact Analysis（2020年12月22日，在投）
欢迎广大学者引用。
