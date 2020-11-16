<font face="Dejavu Sans"/>

# ItC Week 10 - Machine Language

###### tags: `Intro_to_Comp`

- ## Introduction
    - Machine language can be view as a programmer oreiented abstraction of the hardware platform
    - Assembler translate assembly to binary codes

- ## Assembly
    - Insturction
        - Assembly Language : human-readible
        - Machine Language : computer-readible
        - Assembler : translates
    - Example
        - C version
            ```C
            int i = 1;
            int sum = 0;
            while(i<=100){
                sum += i;
                i++;
            }
            ```
        - "Hack" Machine Language version
            ```
                @i
                M=1
                @sum
                M=0
            (LOOP)
                //test if i <= 100
                @i
                D=M
                @100
                D=D-A
                @END
                D;JGT
                //"real" loop content
                @i
                D=M
                @sum
                M=D+M
                @i
                M=M+1
                @LOOP
                0;JMP
            (END)
                @END
                0;JMP
            ```


{%hackmd OQo9p0ONRaSb9WIkZQZZ7w %}