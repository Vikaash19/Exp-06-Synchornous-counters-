# Synchornous-counters - up counter and down counter 
### AIM: 
To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
## THEORY 

### UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



### DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
## Procedure:
~~~
1.Create a new project in QuartusII software.
2.Name the project as uc for upcounter and dc for
down counter.
3.Create a new verilog hdl file in the project file.
4.Name the module as dc and uc for down counter and up counter.
5.Within the module declare input and output variables.
6.Create a loop using if-else with condition parameter as reset value.
7.End the loop. 8.End the module.
~~~
## PROGRAM:
~~~
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Vikaash K S
RegisterNumber: 23013426
~~~
### UP COUNTER:
![up counter code](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/b2d139e0-3ceb-4217-be75-748118df84ef)

### DOWN COUNTER:
![down counter code](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/ec61964d-59ae-4d52-ab0b-c13cc5abd9ec)

## RTL LOGIC UP COUNTER AND DOWN COUNTER  
### UP COUNTER:
![UPCOUNTER RTL](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/007302d6-0895-4462-bc02-5d8e4df64892)

### DOWN COUNTER:
![DOWNCOUNTER RTL](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/1116c274-2f9f-4479-b0f2-bb71e64b4317)

## TIMING DIGRAMS FOR COUNTER: 
### UP COUNTER:
![UP TIME](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/5caac084-8dfb-4964-b868-bb848891f451)

### DOWN COUNTER:
![DOWN TIME](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/d7c05300-81a3-4ca9-9a53-5ef3829d8413)

## TRUTH TABLE: 
### UP COUNTER:
![UP TT TABLE](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/8c76dca4-6f5e-46dc-8713-a20e774fb595)

### DOWN COUNTER:
![DOWN TT](https://github.com/Vikaash19/Exp-06-Synchornous-counters-/assets/148514589/b4e5bfff-6526-4021-bf8b-46e11e500f04)

## RESULT:
Thus Synchornous counters up counter and down counter circuit are studied and the truth table for
different logic gates are verified.
