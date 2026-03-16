# LED-Interfacing-Using-8051

## Aim:
To interface an LED with the 8051 microcontroller and control its operation.

## Apparatus Required:
•	Laptop with Keil uVision software</br>
•	Proteus Design Suite</br>

## Circuit Diagram Setup in Proteus:
1.	Open Proteus and create a new project.</br>
2.	Add the following components from the library:</br>
o	8051 Microcontroller (AT89C51)</br>
o	LED</br>
o	Resistor (330Ω)</br>
o	Ground (GND) connection</br>
3.	Connect the LED's anode to P1.0 of the microcontroller through a 330Ω resistor.</br>
4.	Connect the cathode of the LED to GND.</br>
5.	Save the design and proceed to programming in Keil.</br>

## Algorithm:
1.	Configure P1.0 as an output port.</br>
2.	Set P1.0 HIGH to turn ON the LED.</br>
3.	Introduce a delay.</br>
4.	Set P1.0 LOW to turn OFF the LED.</br>
5.	Introduce a delay.</br>
6.	Repeat the process continuously.</br>


## Program:
```
#include<reg51.h>
void main()
{
unsigned char x,y;
unsigned int i;
P1=0x00;
while(1)
	{   
	x=0x01;
	for(y=0;y<8;y++)	
		{
		P1=x;
    for(i=0;i<60000;i++);
    x=x<<1;
    }			
	}	
}
```
## Output:


## Result:
The LED interfacing with the 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.

