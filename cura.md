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

