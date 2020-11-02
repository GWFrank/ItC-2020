<font face="Dejavu Sans"/>

# ItC Week 7 - ALU

###### tags: `Intro_to_Comp`

- ## Introduction

  - Digital Building Blocks
    - gates, multiplexer, decoder, register etc.

- ## Arithmetic Circuits & Number Systems
  
  - 1-bit Half Adder & Full Adder
    - full adder handles carry-ins
  - **Multibit adder**
    - **Ripple carry adder**
      - really slow
      - $t_{ripple} = N t_{FA}$
      - can be accelerated with parallelizing computation
        - e.g. divide a 16-bit number into 4 blocks of 4-bit numbers
    - **Carry-lookahead Adder**
      - take advantage of *generate* and *propagate* signals
      - *generate* : $G_{i} = A_i B_i$
      - *propagate* : $P_i = A_i +B_i$
      - *carryout* : $C_i = G_i + P_i C_{i-1}$
      - how to add
        1. Compute $G_i$ and $P_i$
        2. Compute $G$ and $P$ for the block
        3. $C_{in}$ of the number propagate through each block
      - $t_{CLA}=t_{pg}+t_{pg\_block}+$
  - Subtracter
    - $Y = A-B =A+B'+1$
  - Comparator (Equality)
    - XOR gate and NOT gate
  - Comparator (less than)
    - use subtracter's output's sign bit
  - **ALU**
    - combines multiple numerical and logical operations into a single unit
    - inside CPU, GPU, FPU...
    - two number inputs $A$ & $B$
    - a input $F$ to decide which calculation result to output
  - Shifter
    - **Logical Shifter**
    - **Arithmetic Shifter**
    - **Rotator**
  - **Multiplier**
    - realized with AND gates and shifters
  - **Integers**
    - Positive Numbers
      - unsigned binary
    - Negative Numbers
      - 2's complement
      - sign/magnitude
  - **Fractions**
    - fixed point
      - binary point fixed
      - e.g. 2's complement, sign/magnitude
    - **Floating Point**
      - $\pm M \times B^E$
        - Mantissa, Base, Exponent
      - Ver. 1
        - 1 bit sign + 8 bits exponent + 23 bits mantissa
      - Ver. 2
        - since every mantissa starts with "1", don't store it
        - 23 bits mantissa $\to$ 23 bits "fraction"
      - Ver. 3 (IEEE 754 standard)
        - add support for negative exponents
        - exponent $\to$ "biased" exponent (+0x7F)
      - Addition
        1. extract
  - Counter
    - +1 on each clock edge
  - Shift Register

- ## Sequential Building Blocks

- ## Memory Arrays

  - Memory types
    - DRAM : Dynamic Random Access Memory
    - SRAM : Static Random Access Memory
    - ROM : Read Only Memory
  - N address bits & M address bits
    - ![Memory Address](https://i.imgur.com/rl7i161.png)
  - DRAM vs SRAM
    - DRAM uses capacitor
    - SRAM uses cross-coupled inverters
    - DRAM is computer's memory sticks (8 ~ 16GB)
    - SRAM is used in CPU's caches (L3 Cache 32 ~ 64MB)


- ## Logic Arrays

{%hackmd BJrTq20hE %}
