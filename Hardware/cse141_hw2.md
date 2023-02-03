# TOP

## Main

### 1
the "rpt" instruction requires two important parameters: [rs] and [branchaddr]. Therefore, its format should fit in the "I" type. Example:
| I-type | Bits | corresponding "rpt"|
| --- | --- | ---|
|OP code | 6 | "rpt"|
|rs | 5 | rs |
|rt | 5 | N/A |
|IMM | 16 | branchaddr

### 2
```
LOOP:   slt $t0, $0, $t1
        beq $t0, $0, Exit
        li  $t0, 1
        sub $t1, $t1, $t0
        j LOOP
DONE:
```
### 3

```
lui $t1, 0X2080
ori $t1, $t1, 0X49A4
```

### 4
The time cycles before using new technology:
$$500*1+300*10+100*3=3800(\text{million cycles})$$
The time cycles after using new technology:
$$500*1*(1-0.5)+300*10+100*3=3550(\text{million cycles})$$
Assume it's 1 unit time per cylce, then the time before using new technology:
$$3800 * 1 = 3800(\text{million unit time})$$
and the time after using new technology:
$$3550 * (1+0.05) = 3727.5(\text{million unit time})$$
And therefore it is a great idea to use the new technology.

### 5
Note the Execution time could be written as:
$$\text{Execution time} = \frac{\text{Number of Cycles}}{\text{Clock Rate}}$$
- When one processor is used:
$$\text{Execution time} = \frac{2.56*10^9+1.28*10^9*20+2.56*10^8*5}{2Ghz} = 14.72s$$
- When two processors are used:
$$\text{Execution time} = \frac{\frac{2.56*10^9}{0.7*2}+\frac{1.28*10^9*20}{0.7*2}+2.56*10^8*5}{2Ghz} = 10.70s$$
$$\text{Speedup} = \frac{14.72}{10.70}=138\%$$
- When four processors are used:
$$\text{Execution time} = \frac{\frac{2.56*10^9}{0.7*4}+\frac{1.28*10^9*20}{0.7*4}+2.56*10^8*5}{2Ghz} = 5.67s$$
$$\text{Speedup} = \frac{14.72}{5.67}=260\%$$
- When eight processors are used:
$$\text{Execution time} = \frac{\frac{2.56*10^9}{0.7*8}+\frac{1.28*10^9*20}{0.7*8}+2.56*10^8*5}{2Ghz} = 3.15s$$
$$\text{Speedup} = \frac{14.72}{3.15}=467\%$$

### 6
Note the Execution time could be written as:
$$\text{Execution time} = \frac{\text{Number of Cycles}}{\text{Clock Rate}}$$
- P1
$$\text{Execution time} = \frac{0.9*5*10^9}{4Ghz} = 1.125s$$
- P2
$$\text{Execution time} = \frac{0.8*1*10^9}{3Ghz} = 0.267s$$
And therefore such fallacy existed, which means that computer with the largest clock rate does not always have the largest performance.

### 7
$$\text{Num of Instructions} = 1.0*10^9 * \frac{0.9}{0.8} *\frac{3}{4}= 0.84 * 10^9$$

### 8 
$$\text{speedup} = \frac{\text{old time}}{\text{new time}} = \frac{300s}{300s-80*0.2}=106\%$$

### 9
$$\text{reduced time needed} = 300s - \frac{300s}{1.25} = 60s$$

### 10
- Machine B
$$\text{Execution time} = \frac{2}{2GHZ} := 1 (\text{unit time})$$
- Machine C
$$\text{Execution time} = \frac{3*1.2}{5GHZ} = 0.72 (\text{unit time})$$

Therefore Machine C is faster and the its speedup over machine B is:
$$\text{speedup} = \frac{0.72s}{1s} = 139\%$$

### 11
- 4-cour
$$\text{speedup} = \frac{1}{0.2+0.8/4} = 2.5$$

- 8-cour
$$\text{speedup} = \frac{1}{0.2+0.8/8} = 3.3$$

### 12
- Sign Extend
$$0000\ 0000\ 0000\ 0000\ 0000\ 0000\ 0010\ 0000$$
- jump “Shift left 2” units
$$0010\ 1001\ 0000\ 0000\ 0000\ 1000\ 0000$$

### 13
$$1010 1100 1010 0100 0000 0000 0010 0000 \to \text{sw \$5 \$4 32}$$
For the ALU, the inputs are the value stored in the source register and IMM, which are $8$ and $32$ respectively.

For PC add unit, the inputs are current PC, which is 0x200000 and $4$.

For Branch add unit, the inputs are 0x200000+4 and 32*4.

### 14
Assume the time to finished a certain number of instructions is 
$$Time_{old} := 1(\text{unit time})$$
Then the time to finished a certain number of instructions after new technology is:
$$Time_{new} = \frac{10-1+3}{10}/\frac{1}{1-10\%} = 1.08(\text{unit time})$$

And thus the speedup would be:
$$\text{speedup} = \frac{1}{1.08} = 93\%$$
Since it's less than one, it's not a good tradeoff.