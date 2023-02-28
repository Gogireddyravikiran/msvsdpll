# 180nm PLL Clock Multiplier IP

# Table of contents
 - [1.Phase Locked Loop](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#1-Phase-Locked-Loop)
 - [2.PLL BLOCK DIAGRAM](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#2-PLL-BLOCK-DIAGRAM)
 - [3.Prelayout Simulations](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#3-Prelayout-Simulations)
 - [4.Specifications](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#-Specifications-)
 - [5.PD(Phase Detector)](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#5-PD(Phase-Detector))
 - [6.VCO(Voltage Controlled Oscillator)](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#6-VCO(Voltage-Controlled-Oscillator))
 - [7.CP(Charge Pump)](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#7-CP(Charge-Pump))
 - [8.Frequency Divider](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#8-Frequency-Divider)
 - [9.PLL](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#9-PLL)
 - [10.Acknowledgements](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#10-Acknowledgements)
 - [11.Contact](https://github.com/Gogireddyravikiran/msvsdpll/blob/main/README.md#11-Contact)

 # 1.Phase Locked Loop

PLL stands for Phase-Locked Loop, which is an electronic circuit that can synchronize its output frequency with an input frequency by adjusting its phase and frequency.

PLLs are commonly used in digital circuits, telecommunications, and radio communication systems. They are used to recover timing and frequency information from a noisy input signal or to generate a stable and accurate clock signal for digital systems.

PLLs consist of a voltage-controlled oscillator (VCO), a phase detector, and a loop filter. The phase detector compares the phase of the input signal with the VCO output signal, and the loop filter adjusts the VCO frequency to minimize the phase error. The output frequency of the VCO is then used as the synchronized output signal.

PLLs have many applications in modern electronics, such as in frequency synthesis, clock generation, and phase modulation/demodulation.


10x PLL Clock Multiplier IP on the SCL 180nm node.

Tested through virtuoso simulations on scl <b>180nm tt corner at room termperature</b>

Generates 10x Multiplied Clock

# 2.PLL BLOCK DIAGRAM

![image](https://user-images.githubusercontent.com/110079770/221420600-607404b2-fbcf-4365-932b-cef8cffd47ec.png)

### 3.Prelayout Simulations
<b> Pre-Layout: </b> <br>

Frequency Obtained for  10Mhz input: &nbsp;&nbsp;&nbsp;100MHz <br>

Duty Cycle obtained: &nbsp;&nbsp;&nbsp; 40.6% at 100MHz

Lock in starts at 3.5ns

3rd-Order Loop Filter used [c1, c2, c3, r1, r2, r3]: &nbsp;&nbsp;&nbsp;355fF, 350fF, 345fF, 490, 490, 490.

### 4.Specifications
<h3> Specifications </h3>

| Parameter | Description | min | typ | max | Unit | Conditions |
| --- | --- | --- | --- | --- | --- | --- |
| VDD | Digital Supply | - | 1.8 | - | V | T = 27C |
| F<sub>CLKREF</sub> | Reference | 10 | - |  | MHz | T = 27C |
| F<sub>CLKOUT</sub> | Output Clock | 100 | - |  | MHz | PLL Mode, T = 27C |
| J<sub>RMS</sub> | Jitter (rms) | - | - | - | ps | PLL_Mode |
| DC | Duty Cycle | 40.6 | - | 50 | % | T = 27C | 
| T<sub>SET</sub> | Settling Time | ~30 | - | ~20 | ns | T = 27C |
| C<sub>L</sub> | Load Capacitance | - | - | - | fF | T = 27C |
| IDD | Supply Current | - | - | - | fF | T = 27C |





# 5.PD(Phase Detector)

A phase detector is a critical component in a phase-locked loop (PLL). The PLL is a control system that generates an output signal that is synchronized with an input signal. The input signal may have a frequency and phase that vary over time, and the output signal generated by the PLL is used to track these variations and maintain synchronization.

The phase detector is responsible for comparing the phase of the input signal and the output signal generated by the PLL. The phase detector generates an error signal that is proportional to the phase difference between the two signals. This error signal is then used by the PLL's control circuitry to adjust the output signal frequency and phase to minimize the phase difference and maintain synchronization.

There are different types of phase detectors used in PLLs, including analog phase detectors, digital phase detectors, and mixers. The choice of phase detector depends on the specific application requirements and the characteristics of the input and output signals.

![image](https://user-images.githubusercontent.com/110079770/219592091-287b9540-b966-4577-878b-411eaaa34976.png)

# Simulated Output 

![image](https://user-images.githubusercontent.com/110079770/219910205-7a4f4b9c-197b-4a22-9198-e2851cb5bcda.png)


![image](https://user-images.githubusercontent.com/110079770/219910273-1c91e4a3-c2c5-4106-aff0-f1a2be9e1ef1.png)



# 6.VCO(Voltage Controlled Oscillator)

VCO stands for Voltage Controlled Oscillator. It is an electronic oscillator that produces an output signal whose frequency can be adjusted by varying an input voltage. VCOs are commonly used in a wide range of electronic applications, such as frequency synthesizers, FM modulators and demodulators, and in various types of communication systems.

A typical VCO consists of a frequency-determining resonant circuit (such as a tank circuit), an amplifier, and a voltage-controlled reactance device (such as a varactor diode). By changing the voltage applied to the reactance device, the resonant frequency of the circuit can be adjusted, thereby changing the frequency of the output signal.

The output frequency of a VCO can be a simple sinusoidal wave or a more complex waveform, depending on the design of the oscillator. VCOs are widely used in electronic music synthesizers to generate various sound waves with different timbres and frequencies.

![image](https://user-images.githubusercontent.com/110079770/219592583-7b3adbac-c411-4786-81bd-ad7c13b7418c.png)


# Simulated Output

![image](https://user-images.githubusercontent.com/110079770/219592905-d53bf438-d52c-418d-ad89-93d8a76c1034.png)




# 7.CP(Charge Pump)

A charge pump is an electronic circuit that converts a DC voltage level to a higher or lower DC voltage level. It works by periodically charging and discharging a capacitor or capacitors to generate a higher or lower voltage than the input voltage.

The basic principle of a charge pump is to use a switching network to transfer charge from one capacitor to another in a sequence that increases or decreases the voltage level. In a step-up charge pump, for example, the input voltage is alternately connected to one capacitor and then another, so that the charge accumulates in a series of capacitors, resulting in a higher output voltage.

Charge pumps are used in a variety of electronic applications, including voltage converters, LCD displays, and flash memory programming. They are popular because they are efficient, low-cost, and simple to implement compared to other voltage conversion techniques.

![image](https://user-images.githubusercontent.com/110079770/218623175-da54c5db-34b4-4859-8ccf-92dd86bf209c.png)

# Simulated Output

![image](https://user-images.githubusercontent.com/110079770/219592730-492dd5d3-b04f-47c1-820a-5b4ea25c2113.png)

# 8.Frequency Divider

A frequency divider is an electronic circuit that takes an input signal of a certain frequency and generates an output signal with a lower frequency. This is accomplished by dividing the input frequency by a fixed integer value, known as the division ratio.

Frequency dividers are used in a wide range of applications, including digital electronics, telecommunications, and instrumentation. They are often used in frequency synthesizers, which are electronic circuits that generate a precise frequency output by combining the output of a frequency divider with a stable reference frequency.

There are several types of frequency dividers, including binary dividers, divide-by-n dividers, and programmable dividers. Binary dividers divide the input frequency by powers of two, while divide-by-n dividers divide the input frequency by a fixed integer value. Programmable dividers, as the name suggests, allow the division ratio to be programmed or changed dynamically.

Frequency dividers can be implemented using a variety of electronic components, such as digital logic gates, flip-flops, and counters. Some modern frequency dividers are also implemented using digital signal processing (DSP) techniques, which can provide greater flexibility and accuracy.

![image](https://user-images.githubusercontent.com/110079770/219916777-5b0ca217-7c74-436a-b288-ed2ac33ac269.png)



# 9.PLL

![image](https://user-images.githubusercontent.com/110079770/219593114-ee1566a0-df3d-46a5-9e03-4398e859b9b7.png)

# Simulated Output

![image](https://user-images.githubusercontent.com/110079770/219919201-7ee25044-8e6e-433f-a187-8e2d552d2cc6.png)



### 10.Acknowledgements

* I thank Mr. Kunal Ghosh, co-founder [VSD](https://www.vlsisystemdesign.com/), for providing me the opportunity to  work on this wonderful project.

### 11.Contact 

* Ravi Kiran Reddy (Author), Mtech ECE - gogireddyravikiranreddy@gmail.com
* Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalghosh@gmail.com

