# Auto-Correlation-and-PSD

### Aim:

Write a program for Autocorrelation anmd PSD of signals in SCILAB and verify Wiener-Khinchin relation.

---

### Apparatus Required:

- Computer with i3 processor
- SCILAB

---

### Theory:

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.

$$PSD = S_{xx}(\omega) = FT[R_{xx}(\tau)] = \int_{-\infty}^{\infty} R_{xx} (\tau) e^{-j \omega t} dt$$

$$ACF = R_{xx}(\tau) = l FT [S_{xx}(\omega)] = \frac{1}{2 \pi} \int_{-\infty}^{\infty} S_{xx} (\omega) e^{j \omega t} d \omega$$

---

### Algorithm:

1. Load or Define the Signal: Input uor time-domain signal.
2. Computa Autocorrelation: Calculate the autocorrelation function of the signal.
3. Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch's periodogram or by using the Fourier transform of the autocorrelation.
4. Plot Results: Visualize the autocorrelation function and PSD.

---

### Procedure:

- Refer Algorithms and write code for the experiment.
- Open SCILAB in System.
- Type your code in New Editor.
- Save the file.
- Execute the code.
- If any error, correct it in code and execute again.
- Verify the generated waveform using Tabulation and Model Waveform.

---

### Program:

```sci
clc
clear all;
pi=3.14;
t=0:0.01:2*pi;
x=cos(19*t); 
subplot(3,2,1); 
plot(x); 
au=xcorr(x,x);
 
subplot (3,2,2); 
plot (au); 
v=fft(au); 
subplot(3,2,3);
plot(abs(v)); 
fw=fft(x); 
subplot(3,2,4); 
plot(fw); 
fw2=(abs(fw)).^2;
subplot(3,2,5); 
plot(fw2);
```

---

### Output:

<img width="1126" height="1280" alt="image" src="https://github.com/user-attachments/assets/590f81f0-d519-41da-9958-9bff03acc777" />

---

### Result:

Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
