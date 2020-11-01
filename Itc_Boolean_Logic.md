<font face="Dejavu Sans"/>

# ItC Week 3~4 - Boolean Logic

###### tags: `Intro_to_Comp`

- ## Introduction
  
  - Specifications for time(clock)

- ## Logic Circuits
  
  - Combiniational Logic
    - memoryless
    - output instantly be effected by current inputs
  - Sequential Logic
    - has memory
    - output be effected by current & previous inputs
  - Combinational Compositions
    - every element is combinational
    - no cyclic path
    - every node is either an input or connect to exactly 1 output

- ## Boolean Equation
  
  - Half Adder
  - Truth Table
  - $+ \rightarrow or$
  - $\cdot \rightarrow and$
  - Sum-of-Products(SOP) Form
    - all equations can be written in SOP form
    - solution is guaranteed but not optimized
  - Producto-of-Sum(POS) Form
    - similar to SOP, solution is guaranteed but not optimized

- ## Boolean Algebra
  
  - Idendity Theorem
    - $B \cdot 1 = B$
    - $B + 0 = B$
  - Null Element Theorem
    - $B \cdot 0 = 0$
    - $B + 1=1$
  - Idempotency Theorem
    - $B \cdot B = B$
    - $B + B = B$
  - Involution Theorem
    - $\overline{\overline B}=B$
  - Complement Theorem
    - $B \cdot \overline B = 0$
    - $B + \overline B = 1$
  
- ## Boolean Theorems of Several Variables
  
  - Commutativity(交換律)
  - Associativity(結合律)
  - Distributivity(分配律)
  - Covering
  - Consensus(共識)
  - De Morgan's Theorem
    - $\overline {ABCD}=\overline A+\overline B+\overline C+\overline D$
    - $\overline {A+B+C+D} = \overline A \cdot \overline B \cdot \overline C \cdot\overline D$
  - Bubble Pushing
    - start pushing from output, then work towards input

- ## From Logic to Gates

  - Circuit Schematics
    - inputs on left(or top)
    - outputs on right(or bottom)
    - gates flow from left to right
    - straight wires are preferred
  - Contention
    - marked as "X"
    - circuit tries to drive output to 1 and 0
  - Tristate Buffer
    | E  | A | Out |
    | -- | - | --- |
    | 0  | 0 | Z   |
    | 0  | 1 | Z   |
    | 1  | 0 | 0   |
    | 1  | 1 | 1   |
  - Busses
    - connect different components in a computer(CPU, GPU, RAM etc.)
    - only one device is active at once
    - tristate buffers are commonly used here
  
- ## K-Maps
  
  - Features
    - Minimize boolean equations graphically by combining terms
    - $PA+P\overline A=P$
    - Can handle up to 4 inputs
  - Rules
    - Bit order in (00, 01, 11, 10), so that adjacent rows/ columns only
      differ in 1 bit
    - Every 1 must be "circled" at least once (can be more than once)
    - Each circle must span $2^x$ squares in each direction
    - Each circle must be as large as possible
    - A "don't care" is only cirlced when it helps minimizing the equation
    - The map can be transform in to a torus(donut shape)

- ## Combinaitonal building blocks
  
  - Multiplexer
    - Select between one of $N$ inputs to output
    - $log_2 N$-bits select input
    - Implementation
      - Logic gates
      - Tristates
    - 4:1 Mutiplexer implementation
      - Logic gates
      - Tristates
      - 2:1 multiplexer
    - Application
      - As a look up table
        - ~~Just plug it in(TM)~~
  - Decoder
    - $N$ inputs, $2^N$ outputs
    - Only outpt HIGH on one output
    - Example
      - memory locator (input = address, output = physical memory)

{%hackmd BJrTq20hE %}
