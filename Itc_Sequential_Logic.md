{%hackmd BJrTq20hE %}

<!-- <link href="https://fonts.googleapis.com/css2?family=Oswald&display=swap" rel="stylesheet">  -->

<font face="Dejavu Sans"/>
<!-- <font face = "Roboto"/> -->
<!-- <font face = "Oswald"/> -->


# ItC Week 4~6 - Sequential Logic
###### tags: `Intro_to_Comp`

- Some Examples
  ---
  - Finite State Machine
  - Markov Model
    - Markov model is one kind
  - Hidden Markov Model
  - RNN & LSTM
  - Sequence to Sequence Model

- Introduction
  ---
  - Some definitions
    - state : 
    - latches and flip-flops :
    - synchronous sequential circuits :


- Latches and Flip-Flops
  ---
  - Bistable Circuit
      - ![Bistable Circuit](https://i.imgur.com/s7WYj8x.png =x120)
      - store 1 bit of state
      - but there are no input to control the state

  - SR(Set/Reset) Latch
    - ![SR Latch](https://cdn.sparkfun.com/assets/learn_tutorials/2/1/6/30-SR-flipflop-circuit.PNG =x120)
    - must avoid $S=R=1$ (cause invalid case like $Q = \overline Q$)

  - D Latch
    - ![D Latch](https://media.geeksforgeeks.org/wp-content/uploads/d_ltch.png =x120)
    - essentialy it is just a modified version of SR latch
    - avoids SR latch's problem

  - D Flip-flop
    - ![D Flip-Flop](https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Negative-edge_triggered_master_slave_D_flip-flop.svg/1200px-Negative-edge_triggered_master_slave_D_flip-flop.svg.png =x120)
    - synchronize with clock at the start of 1
    - only allow $D$ go through when clock go from 0 to 1 (a.k.a."*edge triggered*")
  
  - D Latch v.s. D Flip-flop
    - ![D Latch vs D Flip-flop](https://i.imgur.com/FjzEHb4.png =x250)
    - Be careful with latency in circuits!
  
  - Enabled Flip-flop
    - ![Enabled Flip-flop](https://i.imgur.com/l9kFDFo.png =x120)
    - A multiplexer + A D Flip-Flop
  
  - Resettable Flip-flop
  
  - Settable Flip-flop
  
  - Memory Register
    - Register Implementation

  
    
  
- Synchronous Logic Design
  ---
  - Sequential circuits
    - all circuits that are not combinational
  - System synchronized to the clock
  - Rules
    - each element is either a regster or a combinational circuit
    - contains at least 1 register
    - all element recieve the same clock(no latency)

  

- Finite States Machine
  ---
  - Next state determined by input and current state
  - Moore FSM
    - ![Moore FSM](https://i.imgur.com/4R2mI4P.png =x120)
    - outputs depend on only current state
  - Mealy FSM
    - ![Mealy FSM](https://i.imgur.com/NCRqVfk.png =x120)
    - outputs depend on current state ***and*** inputs
  - **Implementation : Traffic Light**
  - **Implementation : Snail**
    - Moore Machine Approach
    - Mealy Machine Approach 
    - Time Diagram : Moore v.s. Mealy
      - When sychronized to the clock, their outputs might not happen at the same time.
      - Because Moore's output happens when entering the state, it will be a bit slower than Mealy's output, which happens when recieve input.
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
<style>

/* h1 {
    font-family: 'Oswald', sans-serif;
} */

/* h1{
		animation: rainbow 2.5s linear;
		animation-iteration-count: infinite;
} */
h1:hover{
        animation: rainbow 2.5s linear;
        animation-iteration-count: infinite;

}
img.ui-avatar{
  animation: spin 1s linear;
  animation-iteration-count: infinite;
}
/* img{
  transition: all 1s;
}
img:hover{
  animation: zoom 1s;
  animation-fill-mode: forwards;
} */


@keyframes rainbow{
		100%,0%{
			color: rgb(255,0,0);
		}
		8%{
			color: rgb(255,127,0);
		}
		16%{
			color: rgb(255,255,0);
		}
		25%{
			color: rgb(127,255,0);
		}
		33%{
			color: rgb(0,255,0);
		}
		41%{
			color: rgb(0,255,127);
		}
		50%{
			color: rgb(0,255,255);
		}
		58%{
			color: rgb(0,127,255);
		}
		66%{
			color: rgb(0,0,255);
		}
		75%{
			color: rgb(127,0,255);
		}
		83%{
			color: rgb(255,0,255);
		}
		91%{
			color: rgb(255,0,127);
		}  
}  
@keyframes boing {
  15%, 40%, 75%, 100% {
      transform-origin: center center;
  }
  15% {
      transform: scale(1.2, 1.1);
  }
  40% {
      transform: scale(0.95, 0.95);
  }
  75% {
      transform: scale(1.05, 1);
  }
  100% {
      transform: scale(1, 1);
  }
}
@keyframes spin {
    from {
        transform:rotate(0deg);
    }
    to {
        transform:rotate(360deg);
    }
}
@keyframes zoom {

  100% {
    transform: scale(2,2)
  }
}
</style>