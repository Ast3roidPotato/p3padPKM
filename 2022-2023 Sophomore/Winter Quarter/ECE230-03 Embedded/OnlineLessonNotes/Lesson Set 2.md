---
excalidraw-default-mode: view
---

```toc

```

^TOC

<[[|previous]] | [[|next]]>

## Lesson 2-1

Term: PAD the internal circuit that allows the pin to be configured. It drives or interprets the signal.

### Common Pin Configurations
- Push Pull - Used for outputs
- High Impedance - used for inputs
- Open Drain - only capable of driving a LOW signal, otherwise in High - Z mode.
Floating pin - wilding fluctuating voltage.


#### Push Pull 
The push phase connects the pin to power, while the pull phase connects the pin to GND.

#### High Z
Does not impact the circuit it is connected to.

Three implementations:

- Direct signal interpretation: assumes external driver on the circuit that always makes the input a valid input.
- Internal pull up
- Internal pull down
Many microcontrollers have build in internal pullup/pulldown resistors that are configurable.

#### Open Drain

Two States:
- Driving Logic LOW
- Left Floating
This is useful if you want to have multiple pins controlling a single line, where each is able to pull the line low. 


### IO Ports
Peripherals have multiple registers associated with them.
They usually are mapped to be accessible with a normal memory address.

### Bit Masking
It exists. Yay

###  Digital Logic Families
They define standardized voltage levels.

TTL =  Transistor - Transistor Logic
 - Inputs
	- 2 - 5V is HIGH
	- 0-0.8 V is LOW
- Outputs
	- 0-0.4V LOW
	- 2.7-5V

Modern stuff commonly uses CMOS, which generally uses less than 5V Logic.

#### Terms:
- Voh = output high
- Vol = output low
- Vih = input high
- Vil = input low

## Lesson 2-2

### LEDs
Cathodes have shorter led and a flat face.

Digital Output Control:
- Active high = positive logic
- Active Low = negative logic
Interface to LED:
- Directly Driven - sourced or sinked by MC Pin
- Indirectly Driven - Powered by rail.

### Switches



