# GENERATION-AND-DETECTION-OF-FM
## AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## THEORY
  Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
  
  #### FREQUENCY DEVIATION Δf  and MODULATION INDEX m f :
  
  The frequency deviation Δf represents the maximum shift between the  modulated signal
  frequency, over and under the frequency of the carrier.
  
  We define modulation index m f the ratio between Δf and the modulating frequency
  m= Δf / fm


#### FREQUENCY MODULATION GENERATION:
  The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.

## ALGORITHM
  1.	Define Parameters:
     
      •	Fs: Sampling frequency.
      •	T: Duration of the signal.
      •	Fc: Carrier frequency.
      •	Fm: Frequency of the modulating signal.
      •	Beta: Modulation index, which controls the extent of frequency deviation.
  2.	Generate Signals:
     
      •	modulating_signal: Sinusoidal signal used for modulation.
      •	carrier_signal: The high-frequency carrier signal.
      •	modulated_signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
      
  3.	FM Modulation:
     
      •	Modulated_signal is obtained by modulating the carrier signal with the modulating signal.
 
  4.	FM Demodulation:
     
      •	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
      •	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
      •	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
      
  5.	Visualization:
      
      •	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.


## PROCEDURE

    •	Refer Algorithms and write code for the experiment.
    •	Open SCILAB in System
    •	Type your code in New Editor
    •	Save the file
    •	Execute the code
    •	If any Error, correct it in code and execute again
    Verify the generated waveform using Tabulation and Model Waveform

## MODEL GRAPH:
<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/dfe6bc64-2b6f-4afa-ae79-95391859ab04" />

## PROGRAM:
```
Am=19;
Fm=285;
b = 3.8;
Ac=38;
Fc=2850;
Fs=2850000;
t=0:1/Fs:2/Fm;

em = Am*cos(2*3.14*Fm*t);
subplot(3,1,1);
plot(t,em);
xgrid;
ec = Ac*cos(2*3.14*Fc*t);
subplot(3,1,2);
plot(t,ec);
xgrid;
efm = Ac * cos((2*3.14*Fc*t) + ( b*sin(2*3.14*Fm*t)));
subplot(3,1,3);
plot(t,efm);
xgrid;
```

## TABULATION:
![WhatsApp Image 2025-11-21 at 14 03 25_12a8f560](https://github.com/user-attachments/assets/73f414cb-4fa8-4a45-9e49-5455bfdfc385)

## CALCULATION:
![WhatsApp Image 2025-11-21 at 14 00 12_1f7071eb](https://github.com/user-attachments/assets/c3158344-3935-4900-b474-eae67d98116b)

## OUTPUT:
<img width="766" height="445" alt="Screenshot 2025-11-21 134323" src="https://github.com/user-attachments/assets/e0d78713-f14a-47d3-adc3-b5d733b6f8eb" />

## RESULT:
Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.

