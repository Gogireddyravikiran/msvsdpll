# 180nm PLL Clock Multiplier IP

PLL stands for Phase-Locked Loop, which is an electronic circuit that can synchronize its output frequency with an input frequency by adjusting its phase and frequency.

PLLs are commonly used in digital circuits, telecommunications, and radio communication systems. They are used to recover timing and frequency information from a noisy input signal or to generate a stable and accurate clock signal for digital systems.

PLLs consist of a voltage-controlled oscillator (VCO), a phase detector, and a loop filter. The phase detector compares the phase of the input signal with the VCO output signal, and the loop filter adjusts the VCO frequency to minimize the phase error. The output frequency of the VCO is then used as the synchronized output signal.

PLLs have many applications in modern electronics, such as in frequency synthesis, clock generation, and phase modulation/demodulation.


10x PLL Clock Multiplier IP on the SCL 180nm node.

Tested through virtuoso simulations on scl <b>180nm tt corner at room termperature</b>

Generates 10x Multiplied Clock

### PLL BLOCK DIAGRAM

![image](https://user-images.githubusercontent.com/110079770/221420600-607404b2-fbcf-4365-932b-cef8cffd47ec.png)


<b> Pre-Layout: </b> <br>

Frequency Obtained for  10Mhz input: &nbsp;&nbsp;&nbsp;100MHz <br>

Duty Cycle obtained: &nbsp;&nbsp;&nbsp;46% at 40MHz and 40.6% at 100MHz

3rd-Order Loop Filter used [c1, c2, c3, r1, r2, r3]: &nbsp;&nbsp;&nbsp;355fF, 350fF, 345fF, 490, 490, 490.

<h3> Specifications </h3>

| Parameter | Description | min | typ | max | Unit | Conditions |
| --- | --- | --- | --- | --- | --- | --- |
| VDD | Digital Supply | - | 1.8 | - | V | T = 27C |
| F<sub>CLKREF</sub> | Reference | 10 | - |  | MHz | T = 27C |
| F<sub>CLKOUT</sub> | Output Clock | 100 | - |  | MHz | PLL Mode, T = 27C |
| J<sub>RMS</sub> | Jitter (rms) | - | - | - | ps | PLL_Mode |
| DC | Duty Cycle | 52.7 | - | 50 | % | T = 27C | 
| T<sub>SET</sub> | Settling Time | ~37 | - | ~22 | ns | T = 27C |
| C<sub>L</sub> | Load Capacitance | - | - | - | fF | T = 27C |
| IDD | Supply Current | - | - | - | fF | T = 27C |





# PD(Phase Detector)

![image](https://user-images.githubusercontent.com/110079770/219592091-287b9540-b966-4577-878b-411eaaa34976.png)

# Simulated Output 

![image](https://user-images.githubusercontent.com/110079770/219910205-7a4f4b9c-197b-4a22-9198-e2851cb5bcda.png)


![image](https://user-images.githubusercontent.com/110079770/219910273-1c91e4a3-c2c5-4106-aff0-f1a2be9e1ef1.png)



# VCO(Voltage Controlled Oscillator)

![image](https://user-images.githubusercontent.com/110079770/219592583-7b3adbac-c411-4786-81bd-ad7c13b7418c.png)


# Simulated Output

![image](https://user-images.githubusercontent.com/110079770/219592905-d53bf438-d52c-418d-ad89-93d8a76c1034.png)




# CP(Charge Pump)

![image](https://user-images.githubusercontent.com/110079770/218623175-da54c5db-34b4-4859-8ccf-92dd86bf209c.png)

# Simulated Output

![image](https://user-images.githubusercontent.com/110079770/219592730-492dd5d3-b04f-47c1-820a-5b4ea25c2113.png)

# Frequency Divider

![image](https://user-images.githubusercontent.com/110079770/219916777-5b0ca217-7c74-436a-b288-ed2ac33ac269.png)



# PLL

![image](https://user-images.githubusercontent.com/110079770/219593114-ee1566a0-df3d-46a5-9e03-4398e859b9b7.png)

# Simulated Output

![image](https://user-images.githubusercontent.com/110079770/219919201-7ee25044-8e6e-433f-a187-8e2d552d2cc6.png)



<h3> Acknowledgements </h3>

* I thank Mr. Kunal Ghosh, co-founder [VSD](https://www.vlsisystemdesign.com/), for providing me the opportunity to  work on this wonderful project.

<h3> Contact </h3>

* Ravi Kiran Reddy (Author), Mtech ECE - gogireddyravikiranreddy@gmail.com
* Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalghosh@gmail.com
