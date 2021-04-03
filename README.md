# 4_bit_RPN_Calculator
## What I learned
* Implementation a state machine into a schematic
* Handling scheduling for complex multi component operations
* Working around hardware limitations, by modyfying chips to work in a manner different than intended
* Working with Ram chips and using them to implement a Stack
* Performing basic arithmetic algorithims using ALU's
 A multisim project using counters, multiplexers, RAM chips, and ALUs, to implement a state machine creating an RPN calculator
 Design consists of a control unit used for handling input and scheduling operations, and a seperate section for execution of 
 operations and storage of data.
## Control unit
* Consists 2 four bit input switches X and Y with x representing the number loaded and y the operation desired
* Also contains 2 other switches one labvelled push to actually load the number onto the stack and func to execture the operation
* Utilizes 2 counters and a series of logic gates to function as the different states needed for logical operation for the operational hardware
## Operational unit
* Uses a counter to send correct memory address to RAM chip in order to ensure proper stack behavior, utilizing a combination of logic gates to load previous value
* Ram chip is used to store numbers directly sent through control unit and operational results onto a stack
* Registers are used to temporarily hold first output from ram as it can only output one value at a time, and to ensure only new operations are sent to output
* ALU is used for Arithmetic operations
* MUX is used to decide whether to load number from control unit or results of an arithemtic operation.
## Operation instructions
1. First load binary number on x switches
2. close the push switch and then quickly release
3. Repeat steps 1 and 2 again for second number
4. Input in the desired output function according to chart located in page of the lab report
5. close the func switch and then quickly release
6. Output will be shown on thje QD,QC,QB,QA LED's
7. repeat as desired ensuring at least 2 items on the stack

