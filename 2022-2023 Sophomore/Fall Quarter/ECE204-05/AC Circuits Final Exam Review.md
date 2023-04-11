### Topics:
- 2 Problems from Exam 1
- 2 Problems from Exam 2
- 1 Problem with Self/Mutual Inductance
- 1 Problem on transformers


### Example Problem Types:
1. GIVEN: A waveform
	FIND: $V=L\frac{di}{dt},\qquad W=\frac{1}{2}Li^2$
	$\quad\;\;\; i=C\frac{dv}{dt},\qquad W=\frac{1}{2}CV^2$
2. GIVEN: A parametric circuit
	FIND: Solve the circuit in the phasor domain, etc.
3. GIVEN: Time expression for voltages of a 3-Phase Circuit
	FIND: Phasor diagram, line-line voltages, balanced or unbalanced, $\pm$ or $-$ phase sequence.
4. GIVEN: 3-Phase Y or $\Delta$ power system
	FIND: Phase voltages, line voltages, phase currents
5. GIVEN: Circuit with mutual coupling $M$
	FIND: Write differential equations, plug-in the solution to verify you equations are correct, find the voltages in the circuit.
6. GIVEN: Transformer test results
	FIND: EQ Circuit Parameters and %V.R. and $\eta$

### Content
#### Exam 1 Topics:
- Simplifying capacitor/inductor networks
- RMS conversions
- Phase angles from equations
- Phasor diagrams
- Figuring out the impedance of load based on equations
- Norton/Thevenin equivalents
- Mesh Current and Node Voltage with phasor values

#### Exam 2 Topics:
- Real, Reactive, Complex, Apparent power from equations
- Average and reactive power from circuit 
	 - IMPORTANT: ![[2022-2023 Sophomore/Fall Quarter/ECE204-05/Notes/2022-10-26#Important!|Review this!]] Power Equation Rules
- get P, W, S and PF from $S,V,\theta$
- Power factor correction capacitors calculations.
- Power triangle 
- Voltage regulation and efficiency $(\eta)$
- Y vs $\Delta$ loads
- Line-Line vs Phase voltage at source and load
- Line currents in delta and wye configurations

#### Mutual Inductance - Lectures 23 - 24
- Dots indicating coil position / coil wrap
	- When current enters the dotted terminal of a coil, it induces a <u>positive</u> voltage in the other coil at the doted terminal.
- $L$ is referred to as self-inductance.
- Two circuits that are linked by a magnetic field have $L_1, L_2, M$ where $M$ is the mutual inductance. By treating $M$ as a separate inductance value, there are 2 voltages induced over each coil. One from self-inductance and one for mutual inductance.
![[Pasted image 20221113170236.png|500]]
![[Pasted image 20221113170252.png|500]]
- Faraday's Law
- Coupling Coefficient $k$
- $M = k\sqrt{L_1L_2}$


#### Transformer Stuff - Lectures 25 - 29
- IDEAL TRANSFORMER:
		- ![[Pasted image 20221113175413.png]]
	- Assuming that both coils have zero series resistance: $Z_{ab} = (\frac{N_1}{N_2})^2(R_L+jX_L)$
	- ![[Pasted image 20221113175655.png]]
	- $\frac{1}{a} = \frac{N_1}{N_2}$
	- $\frac{V_1}{V_2} = \frac{I_2}{I_1} = \frac{N_1}{N_2}$
	- Properties:
		- No flux leakage
		- The winding resistance is zero
		- The core has infinite permeability
		- The magnetic core is lossless
- REAL TRANSFORMER
	- The transformer models have one side that is an ideal transformer half. This side can be either primary or secondary
	- ![[Pasted image 20221113180504.png]]
		- $E_1$ - Primary induced voltage
		- $E_2$ - Secondary induced voltage
		- $V_1$ - Primary terminal voltage
		- $V_2$ - Secondary terminal voltage
		- $I_1$ - Primary current
		- $I_2$  - Secondary current
		- $I_e$ - Excitation Current
		- $I_m,X_m$ - Magnetizing current and reactance
		- $I_c,R_c$ - Core loss current and resistance
		- $R_1$ - Resistance of the primary winding
		- $R_2$  - Resistance of the secondary winding
		- $X_1$ - Primary leakage reactance
		- $X_2$ - Secondary leakage reactance
	- Simplified Model:
		- ![[Pasted image 20221113181155.png]]
	- Super Simplified Model:
		- ![[Pasted image 20221113181216.png]]
	- IMPORTANT PLUG'N'CHUG EQUATIONS FOR EQUIVALENT CIRCUIT PARAMETERS
	- Open Circuit Test
		- Apply the rated input voltage to the (low side of the)  transformer and leave the output (high side) open
		- Measure *power, voltage, and current* on the input (low) side.
		- The current $I_{oc}$ is the *exiting current* through the shunt excitation branch
		- $Y$ is admittance, which is the opposite of $Z,$ impedance 
		- $G$ is conductance, which is the opposite of $R,$ resistance
		- $B$ is susceptance, which is the opposite of $X,$ reactance
		- $|Y_{o2}| = \frac{I_{oc}}{V_{oc}}$
		- $\theta_{o2} = \cos^{-1}({\frac{P_{oc}}{V_{oc}\cdot I_{oc}}})$
		- $Y_{o2} = |Y_{o2}|\angle{-\theta_{o2}} = G_{c2} - jB_{m2}$
		- Values on the opposite (primary) side are:
			- $R_{c1} = a^2R_{c2}$
			- $X_{m1} = a^2X_{m2}$
		- Input power is essentially the rated core loss, which is assumed to remain constant.
	- Short Circuit Test
		- The output side (low voltage side) is short circuited and the input side (high voltage) is connected to a variable low voltage source.
		- The input power, voltage and current are measured.
		- The applied input voltage is smaller than the rated voltage in order to avoid burning out the secondary.
		- When this is done, the current through the magnetizing (shunt???) branch is negligible.
			- Therefore the applied voltage is practically equal to the voltage drop across the transformer series impedance.
		- $|Z_{e1}| = \frac{V_{sc}}{I_{sc}}$
		- $R_{e1} = \frac{P_{sc}}{I_{sc}^2} + a^2R_2$
		- $X_{e1} = \sqrt{|Z_{e1}|^2-R_{e1}^2} = X_1 + a^2X_2$
		- Values on the opposite (secondary side) are:
			- $R_{e2} =(\frac{1}{a^2})R_{e1}$
			- $X_{e2} = (\frac{1}{a^2}X_{e1})$
	- Notes on 3-Phase
		- These tests work on 3-Phase transformers
		- Measured power is full 3-phase power
		- Measured voltage is line-to-line voltage
		- To use the formulas, convert the values to per-phase values before proceeding.
- Voltage Regulation
	- The value of the secondary voltage is a function of the current drawn by the load
	- This is due to the voltage drop across the internal impedance of the transformers.
	- The measure of how much the voltage will change as a load is varied is called *voltage regulation.*
	- The *voltage regulation* is defined as the change in the magnitude of the *secondary voltage* as the current change from *full load* to *no load* with the primary voltage held constant.
- Efficiency
	- The percent *efficiency* of a transformer is the ratio of *output power* to *input power.*

Lecture 30 has some op-amp stuff??

### Equations To Put On Sheet

#### Exam 1:
- $V = L\frac{di}{dt}$
- $i(t) = \frac{1}{L}\int{Vdt} + i(0)$
- $W = \frac{1}{2}Li^2$
- $i = C^2\frac{di}{dt}$
- $V(t) = \frac{1}{C}\int{idt} + V(0)$
- $W = \frac{1}{2}CV^2$
- $V_m = peak$
- $\omega = 2\pi f = \frac{2\pi}{T}$
- $\sin(x) = \cos(x-90^\text{o})$
#### Exam 2:
- 

#### Mutual Inductance & Transformers