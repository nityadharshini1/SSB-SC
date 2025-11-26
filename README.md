# SSB

EXP NO: 3	SSB-SC-AM MODULATION using SCILAB

AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

Note: Keep all the switch faults in off position


Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: The baseband signal that will be modulated.
•	Carrier Signal: A high-frequency signal used for modulation.
•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
3.	SSBSC Modulation:
•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
4.	SSBSC Demodulation:
•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
5.	Visualization:
•	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.


PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="704" height="178" alt="image" src="https://github.com/user-attachments/assets/32ee29b3-0d95-4192-9762-972d50c05c90" />
<img width="706" height="167" alt="image" src="https://github.com/user-attachments/assets/bff0d8fd-d679-444e-af37-0b34585853c1" />

Program

'''clc;
clear all;
close all;

Am = 8.9;
fm = 370;
Ac = 17.8;
fc = 10000;
fs = 100000;

t = 0:1/fs:0.01;

m = Am*cos(2*pi*fm*t);
mh = imag(hilbert(m));

c = cos(2*pi*fc*t);
s = sin(2*pi*fc*t);

s_usb = Ac*(m.*c - mh.*s);
'''

figure;
subplot(3,1,1); plot(t,m); title('Message Signal'); grid on;
subplot(3,1,2); plot(t,mh); title('Hilbert Transform'); grid on;
subplot(3,1,3); plot(t,s_usb); title('SSBâ€‘SC USB Signal'); grid on;

OUTPUT WAVEFORM
![WhatsApp Image 2025-11-26 at 08 12 33_64b2809e](https://github.com/user-attachments/assets/a1a03bc9-a70e-4196-b2d8-7589053d8e6b)

TABULATION
![WhatsApp Image 2025-11-26 at 08 12 32_74c8f5a1](https://github.com/user-attachments/assets/f644fff7-5075-4243-b942-280f7fe45e95)









RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





