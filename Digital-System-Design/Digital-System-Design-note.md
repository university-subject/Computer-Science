# Digital System Design 數位系統設計

collected & noted by JingShing

## 參考書目：

1.數位邏輯設計與晶片實務，劉紹漢，全華

2.FPGA/CPLD可程式化邏輯設計實習：使用VHDL與Terasic DE2，宋啟嘉，全華

## 第一章 數位邏輯電路的沿革,實現與硬體描述語言 HDL

### 數位邏輯電路設計的沿革

### 五個階段：

1. 小型積體電路 ( SSI )

2. 中型積體電路 ( MSI )

3. 大型積體電路 ( LSI )

4. 超大型積體電路 ( VLSI )

5. 極大型積體電路 ( ULSI )

### 小型積體電路 SSI

#### 設計一個 2 對 4 高態動作的解碼器

```VHDL
library IEEE;
use IEEE.std_logic_1164.all;

entity dmuxto16 is
	Port (Din:in std_logic;
			S:in std_logic_vector(3 downto 0);
			F:out std_logic_vector(15 downto 0)
	);
end dmuxto16;

architecture dmuxto16 of dmuxto16 is
	signal P:std_logic_vector(3 downto 0)
begin
	P(0) <= Din when S(3 downto 2) = "00"
end dmuxto16;
```
