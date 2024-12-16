# 24V->12V降圧DCDC基板
> 茨城高専BチームR1(高専ロボコン2024)に搭載された降圧DCDC基板
> ROHM製 BD9F800MUX-Zを使用

## 概観
**スケッチ**
![image of schematic](figures\sch.png)
**実体配線**
![image of pcb](figures\pcb.png)
**実装した図**
![implemented](figures\real.jpg)

## 目的
- 24V駆動電源から12V 8Aを生成し、12Vを用いる制御機器に分配する

## 仕様
- **BD9F800MUX-Z**
	- [データシート](https://fscdn.rohm.com/jp/products/databook/datasheet/ic/power/switching_regulator/bd9f800mux-j.pdf?_fsi=rojoN0SD)
	- $F_{osc}$ = 600khz
	- $V_{max}$ = 28V
	![BD9F800MUZ-Z in schematic](figures\BD9F800MUX-Z.png)
- ヒューズ破壊式逆接保護
	- SBD: [BR310_R1_00001](https://www.digikey.jp/short/h203d347)
	![protect from reverse connection](figures\protect.png)