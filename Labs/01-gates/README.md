# Digital-electronics-1
## Lab 1
### 1)
Môj github link: https://github.com/xsebov01/Digital-electronics-1 

### 2) Dôkaz DeMorganových pravidiel
Eda playground link: https://www.edaplayground.com/x/G2BJ

| **c** | **b** |**a** | **f(c,b,a)** |
| :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |


**Source code**

```vhdl
architecture dataflow of gates is
begin
    f_o     <= (not b_i and a_i) or (not c_i and not b_i);
   	fnand_o <= not (not (not b_i and a_i) and not(not b_i and not c_i));
  	fnor_o  <= not (b_i or not a_i) or not (c_i or b_i);
  
end architecture dataflow;
```
**Screenshot**




### 2) Dôkaz distributívnych pravidiel

Eda playground link: https://www.edaplayground.com/x/BAAq

**Source code**

```vhdl
architecture dataflow of gates is
begin
    f11_o     <= ((a_i and b_i) or (a_i and c_i));
    f12_o     <= (a_i and (b_i or c_i));
    f21_o     <= ((a_i or b_i) and (a_i or c_i));
    f22_o     <= (a_i or (b_i and c_i));
    
end architecture dataflow;
```
**Screenshot**


