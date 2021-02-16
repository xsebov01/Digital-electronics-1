# Digital-electronics-1
## Lab 1
### 1)
Môj github link: https://github.com/xsebov01/Digital-electronics-1 

### 2) Dôkaz DeMorganových pravidiel
Eda playground link:

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
