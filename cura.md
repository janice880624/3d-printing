# Cura

### 👉下載軟體

{% hint style="success" %}
軟體下載[https://ultimaker.com/software/ultimaker-cura](https://ultimaker.com/software/ultimaker-cura)
{% endhint %}

![](.gitbook/assets/image%20%2855%29.png)

### 👉新增印表機

#### step 1. 點選【新增印表機】

![](.gitbook/assets/image%20%2819%29.png)

#### step 2. 新增【非網路】印表機 ➡ Creality3D ➡ Creality Ender-3

![](.gitbook/assets/image%20%288%29.png)

#### step 3. 設置基本參數 \(請先參考下面設置\)

![](.gitbook/assets/image%20%2825%29.png)

```text
// 起始G-code
; Ender 3 Custom Start G-code
G92 E0 ; Reset Extruder
G28 ; Home all axes
G1 Z2.0 F3000 ; Move Z Axis up little to prevent scratching of Heat Bed
G1 X0.1 Y20 Z0.3 F5000.0 ; Move to start position
G1 X0.1 Y200.0 Z0.3 F1500.0 E15 ; Draw the first line
G1 X0.4 Y200.0 Z0.3 F5000.0 ; Move to side a little
G1 X0.4 Y20 Z0.3 F1500.0 E30 ; Draw the second line
G92 E0 ; Reset Extruder
G1 Z2.0 F3000 ; Move Z Axis up little to prevent scratching of Heat Bed
G1 X5 Y20 Z0.3 F5000.0 ; Move over to prevent blob squish
```

```text
// 結束G-code
G91 ;Relative positioning
G1 E-2 F2700 ;Retract a bit
G1 E-2 Z0.2 F2400 ;Retract and raise Z
G1 X5 Y5 F3000 ;Wipe out
G1 Z10 ;Raise Z more
G90 ;Absolute positionning

G1 X0 Y{machine_depth} ;Present print
M106 S0 ;Turn-off fan
M104 S0 ;Turn-off hotend
M140 S0 ;Turn-off bed

M84 X Y E ;Disable all steppers but Z
```

### 👉介面介紹

![](.gitbook/assets/image%20%2863%29.png)

* 工作平台選項➡選擇 3D列印機、面板配置、列印設定

### 👉 填充密度

**填充密度會影響列印件的強度和重量**

![](.gitbook/assets/image%20%2867%29.png)

![](.gitbook/assets/image%20%2870%29.png)

### 👉 切層厚度

**切層厚度會影響列印成品的細緻程度**

![](.gitbook/assets/image%20%2868%29.png)

![](.gitbook/assets/image%20%2865%29.png)

### 👉 支撐

**根據列印品去選擇是否開啟支撐**

![](.gitbook/assets/image%20%2864%29.png)

### 👉 筏板

這個底座的目的是希望讓3D模型可以更好地粘貼在打印平台上，防止3D模型出現翹邊的問題。另一方面，如過模型底部的面積很小的話，加上raft後也可以增強這個模型粘貼在打印平台上的程度。一般來講當3D打印完畢以後，只有把模型底部的raft直接移除就搞定。

![](.gitbook/assets/image%20%2871%29.png)



### 👉 附著

{% hint style="info" %}
更多參數設定[https://3dmart.com.tw/news/ultimaker-cura2.1-printing-software-guide](https://3dmart.com.tw/news/ultimaker-cura2.1-printing-software-guide)
{% endhint %}

{% hint style="info" %}
故障排除參考[https://z3dfilament.blogspot.com/2019/01/3dproblem.html](https://z3dfilament.blogspot.com/2019/01/3dproblem.html)
{% endhint %}

