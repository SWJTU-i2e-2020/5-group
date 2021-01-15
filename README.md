# 5-intelligence-agriculture
## 项目名称：二氧化碳浓度监测仪
作者 | github ID
---------- | -------------
颜海月 | haiyue-yan
刘倚赫 |	YiHe-Liu
马姣姣 |	Gioia-Ma
杨弘毅 |	Hongyi-Yangz
李芋霖 |	linyu-lee
朱语 |	520zy520

## 一、问题定义
### （1）需求介绍及分析
&#8195;&#8195;CO2浓度对农作物生长具有非常大的影响。当塑料大棚内二氧化碳浓度过低或过高时，会影响塑料大棚作物产量。在塑料大棚中安装二氧化碳监测仪可以保证在二氧化碳监测仪浓度
过高或过低的情况下及时报警，从而使用气肥或通风通气。保证蔬菜、食用菌、鲜花、中药等提早上市、高质高产。
### （2）需求列表 
| Want | Wish |
| :--- | :--- |
| 实时测量CO2浓度 | 显示值达到较高的精度及刷新率 |
| 设置阈值，超出警报 | 实现远程接收警报 |
| 外观实用耐磨损 | 实现美观 |
| 尺寸合理 | 达到便携 | 
| 便于生产维护 | 达到低成本，高效率 |
| 具有较长的生命周期 |同时达到低功耗，高稳定性 |
### （3）产品总体功能
&#8195;&#8195;我们的大棚二氧化碳监测反馈装备的主要功能是，在大棚中检测出二氧化碳浓度，能够实时显示并远程显示，超标时在实地与远程端同时发出报警，从而管理人员发现问题并作出调整。
### （4）指标、特点
| 指标 | 特点 |
| :--- | :---|
| 精度 | 高精度性 |
| 成本 | 低成本性 |
| 操作 | 简易、远近可操作性 |
| 成本 | 低成本、易维护性 |
| 使用寿命 | 功耗低、生命周期长|
| 尺寸 | 小巧易携 |  
## 二、概念设计
| 概念 |  概念草图及介绍  |
|  ------------  |  -----------  |
|  CO2浓度监视器  |  [提取码: rquc](https://pan.baidu.com/s/1fE2-dRpwdXBkVxVm5pLW_w)  |  
|  可实现远程监测的检测系统  |  [提取码：mue7](https://pan.baidu.com/s/1D0fw4ZSlolLxLa11EVaqEg)  |
## 三、详细设计
### 物料清单
| 序号 | 名称 | 型号/规格 | 封装 | 用量 | 品牌 | 商品编号 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 1 | 二氧化碳传感器 | CCS811空气质量测量传感器 | 单独IC封装，15.24mm×15.24mm×2mm | 1 | 维特智能 | 911141 |
| 2 | 电磁式有源一体蜂鸣器5V | YS-MBZ12095DYB05 | Through Hole,12x9.5mm | 2 | Fengming(锋鸣电子) | C409831 |
| 3 | 灯带 | ws2812 |
| 4 | OLED显示模块 | QG-2832TSWFG02 | 0.91"128x32 | 2 | 全智景Allvision | C91219 |
| 5 | 亚克力板 |  | 500mm×500mm×2mm  | 1 |  |  |
| 6 | 2.54杜邦线母对母单P同向(黑) | S108520012 | - | 15 | Ckmtw(灿科盟) | C368924 |
| 7 | esp32 | NodeMCU-32SLua | - | 2 | Ai-Thinker(安信可) | C111436 |
| 8 | Lora | Ra-02/0.91 | Module | 1 | Ai-Thinker(安信可) | C90039 |
### 加工制作过程
[制作过程](https://zaowu.fun/p/600049a236531447f6c5b4b5)
## 四、性能指标
### 外观
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们的产品的外包装是使用牢固轻便的亚克力板拼装粘黏而成的长方体，尺寸是15cm×12cm×8cm。在外包装表面开有必要的孔洞用于暴露Lora的天线，显示屏与蜂鸣器。内部部件均用胶水粘好，牢固无松动。
### 供电方式
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;供电方式采用在产品内置额定容量6000mA·h（5V/2.1A）的充电宝直接供电。
### 功耗
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;查阅资料，ESP32自身CPU工作状态功耗约为20mA-30mA，算上外围芯片，我们产品的正常工作时的功耗在100mA左右。
### 使用时间
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;充电宝一次充满电后保持我们的产品工作状态，可以维持6000mA·h ÷100mA = 60个小时。
### 环境影响
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;温度：一般种植期间大棚（管理得当）内的温度高可达36℃，低可达3℃。在这种温度条件下，我们的产品完全可以正常使用较长时间。</br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;湿度：一般大棚内空气相对湿度可以达到50%-60%，极限情况下可达到100%。我们的产品不完全密封，受湿度影响会较大，导线暴露出的部分与各部件暴露出的接口都会产生金属腐蚀，但仍能使用较长一段时间。</br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;电磁干扰：我们产品受电磁干扰影响较大，无论是自身的正常运行，还是远程传输信号，都会受到影响。不过在大棚地产生电磁干扰的物质较少，实际影响会较少。
### 有毒物质
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;可更换的充电宝自身具有毒性，但对大棚环境不造成影响；产品各个组成部分均封在包装内，不排出有毒物质。
### 灵敏度
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在测试过程中，在较短时间内(<0.5s)反映出二氧化碳浓度变化，对于大棚内蔬菜来说这样的灵敏度完全足够。

## 五、代码
// 节点代码如下：

#include <LoRaNow.h>  //LoRa需要的头文件

#include <Wire.h>     //OLED需要的头文件

#include "SSD1306.h"   //OLED需要的头文件

#include "Adafruit_CCS811.h"//ccs811需要的头文件

Adafruit_CCS811 ccs;

SSD1306 display (0x3c, 21, 22);

#define MISO 19

#define MOSI 23

#define SCK 18

#define SS 5

#define DIO0 4

#define tmpADPin 35

int tmp;

void setup() {

  Serial.begin(9600);
  
  Serial.println("LoRaNow Simple Node");
  
  pinMode(tmpADPin,INPUT);
  
  display.init();
  
  display.setFont(ArialMT_Plain_24);
  
  display.drawString(0, 0, "CO2Monitor"); //显示二氧化碳检测器字样
  
  display.display();
  
   LoRaNow.setFrequencyCN(); 
   
   LoRaNow.setPinsSPI(SCK, MISO, MOSI, SS, DIO0); // Only works with ESP32
   
  if (!LoRaNow.begin()) {
  
   Serial.println("LoRa init failed. Check your connections.");
    
   while (true);
    
  }


  LoRaNow.onMessage(onMessage);
  
  LoRaNow.onSleep(onSleep);
  
  LoRaNow.showStatus(Serial);
  
}


void loop() {

  bool alert;
  
  tmp = CO2();
  
  String myc="  ";
  
  myc.concat(tmp);  				//将数字转化为字符串
  
  myc+="ppm";
  
  display.drawString(0, 0, myc);  	/*显示CO2浓度*/
  
  LoRaNow.loop();
  
  if(tmp>1600)          /*CO2超标警报*/
  
   alert=1;			//上限设置为1600ppm，是否科学有待考证
    
  else
  
   alert=0;
    
}


int CO2() //二氧化碳浓度函数,若二氧化碳浓度不准确，可在函数中进行修正

{
  int nongdu=ccs.geteCO2();
  
  return nongdu;
  
}


void onMessage(uint8_t *buffer, size_t size)

{

  Serial.print("Receive Message: ");
  
  Serial.write(buffer, size);
  
  Serial.println();
  
  Serial.println();
  
}

void onSleep()

{

  Serial.println("Sleep");
  
  Serial.println(tmp);
  
  delay(500); // "kind of a sleep"
  
  Serial.println("Send Message");
  
  LoRaNow.print("LoRaNow Node Message ");
  
  //Serial.println("LoRaNow Message sended");
  
  LoRaNow.print(millis());
  
  LoRaNow.print("-");
  
  LoRaNow.print(tmp);
  
  LoRaNow.send();
  
}


网关代码仍沿用期中的代码



## 六、代码如何运行

### 一、开发者开发环境：

   软件:Arduino,硬件esp32, LoRa, ccs811, oled等。

1.  Arduino中开发板管理器中下载esp32并在开发板中选择ESP32 Dev Module。 


  ![1](https://github.com/SWJTU-i2e-2020/5-intelligence-agriculture/blob/main/images/6.1.png)
  
  ![2](https://github.com/SWJTU-i2e-2020/5-intelligence-agriculture/blob/main/images/6.2.png)
    
  ![3](https://github.com/SWJTU-i2e-2020/5-intelligence-agriculture/blob/main/images/6.3.png)
  
  
2. 在库管理器中安装：WIFI, SSD1306, Adafruit CCS811 Library, LoRaNow, PubSubClient等库。即代码中各种头文件。

  
    ![4](https://github.com/SWJTU-i2e-2020/5-intelligence-agriculture/blob/main/images/6.4.png)
    
    
    ![5](https://github.com/SWJTU-i2e-2020/5-intelligence-agriculture/blob/main/images/6.5.png)
  
  
3. 将设备连入电脑。

4. 将代码复制到Arduino中，上传即可。

5. 在串口监视器9600波特率下能够看见输出的二氧化碳浓度。同时OLED屏幕上也能够显示出对应的数值。

6. 对网关进行同样的操作。

7. 完成上述步骤即完成了二氧化碳监测器的搭建。

8. 当网关和节点同时工作时即可完成二氧化碳浓度的远程监测。

### 二、对于产品使用用户：

1. 本产品已经将代码写入esp32，用户只需要将检测仪器放到需要检测的位置，无需其他任何操作。即可在节点的OLED获取相应信息，也可在网关处获得信息。当二氧化碳浓度超过一定限度时，网关和节点的蜂鸣器会同时报警。发出声音和产生亮光。

2. 在正式的产品内部，含有一个充电宝。当网关处无法得到信息时，考虑是否节点处电量耗尽。可直接从外部接线向充电宝充电。电量充满以后节点可继续使用。

