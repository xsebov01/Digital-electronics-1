# Digital-electronics-1
## Lab 4
### 1) Preparation tasks
| Hex | Inputs | A | B | C | D | E | F | G |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0000 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |
| 1 | 0001 | 1 | 0 | 0 | 1 | 1 | 1 | 1 |
| 2 | 0010 | 0 | 0 | 1 | 0 | 0 | 1 | 0 |
| 3 | 0011 | 0 | 0 | 0 | 0 | 1 | 1 | 0 |
| 4 | 0100 | 1 | 0 | 0 | 1 | 1 | 0 | 0 |
| 5 | 0101 | 0 | 1 | 0 | 0 | 1 | 0 | 0 |
| 6 | 0110 | 0 | 1 | 0 | 0 | 0 | 0 | 0 |
| 7 | 0111 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |
| 8 | 1000 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 9 | 1001 | 0 | 0 | 0 | 0 | 1 | 0 | 0 |
| A | 1010 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| b | 1011 | 1 | 1 | 0 | 0 | 0 | 0 | 0 |
| C | 1100 | 0 | 1 | 1 | 0 | 0 | 0 | 1 |
| d | 1101 | 1 | 0 | 0 | 0 | 0 | 1 | 0 |
| E | 1110 | 0 | 1 | 1 | 0 | 0 | 0 | 0 |
| F | 1111 | 0 | 1 | 1 | 1 | 0 | 0 | 0 |

| Cathode/Anode name | Connection |
| :-: | :-: |
| AN0 | J17 |
| AN1 | J18 |
| AN2 | T9 |
| AN3 | J14 |
| AN4 | P14 |
| AN5 | T14 |
| AN6 | K2 |
| AN7 | U13 |
| CA | T10 | 
| CB | R10 | 
| CC | K16 | 
| CD | K13 | 
| CE | P15 | 
| CF | T11 | 
| CG | L18 | 
| DP | H15 |

### 2) Seven-segment display decoder
**VHDL architecture from source file hex_7seg.vhd**
```vhdl
architecture Behavioral of mux_2bit_4to1 is
begin
    f_o <= a_i when (sel_i = "00") else
           b_i when (sel_i = "01") else
           c_i when (sel_i = "10") else
           d_i;
end architecture Behavioral;
```
**VHDL stimulus process from testbench file tb_hex_7seg.vhd**
```vhdl
architecture Behavioral of mux_2bit_4to1 is
begin
    f_o <= a_i when (sel_i = "00") else
           b_i when (sel_i = "01") else
           c_i when (sel_i = "10") else
           d_i;
end architecture Behavioral;
```

**Screenshot with simulated time waveforms**
![Simulation](images/simulation.png)

**VHDL code from source file top.vhd**
```vhdl
architecture Behavioral of mux_2bit_4to1 is
begin
    f_o <= a_i when (sel_i = "00") else
           b_i when (sel_i = "01") else
           c_i when (sel_i = "10") else
           d_i;
end architecture Behavioral;
```
### 3) LED(7:4) indicators

| **Hex** | **Inputs** | **LED4** | **LED5** | **LED6** | **LED7** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0000 |  |  |  |  |
| 1 | 0001 |  |  |  |  |
| 2 |      |  |  |  |  |
| 3 |      |  |  |  |  |
| 4 |      |  |  |  |  |
| 5 |      |  |  |  |  |
| 6 |      |  |  |  |  |
| 7 |      |  |  |  |  |
| 8 | 1000 |  |  |  |  |
| 9 |      |  |  |  |  |
| A |      |  |  |  |  |
| b |      |  |  |  |  |
| C |      |  |  |  |  |
| d |      |  |  |  |  |
| E | 1110 |  |  |  |  |
| F | 1111 |  |  |  |  |

**Screenshot with simulated time waveforms**
![Simulation](images/simulation.png)








