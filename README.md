# AM-DSB-SSB-Modulations
## Amplitude Modulation
* <p align="justify"> Write a function that takes the message signal $x_{m}(t)$ , carrier wave amplitude $A_c$ , modulation index $\mu$ and carrier wave frequency $f_c$ as input and returns the modulated signal. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/94344f17-7790-44b6-9a2a-2e4aac26adbd)

Now, consider the message signal as follows:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/eae044b0-01ea-412a-b1aa-d201a9ec739d)

* Modulate the message signal with the frequency $f_c = 50Hz$ , $\mu = 0.85$ and $t_0 = 0.15$ and plot the modulated signal.

<p align="justify"> We form the given message signal as follows in the code. It should be noted that the sampling frequency is set to a value that respects the Nyquist rate. For this purpose, the sampling frequency must be greater than 2 times the carrier frequency, i.e. greater than 500 Hz, where we have considered the sampling frequency to be 1000 Hz. We normalize this signal first and plot it. By placing the message signal in the AM modulation relationship, we will have. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/5a1775c1-c836-4ff5-8005-bcbafca8bb3c)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/2a0f8385-47b0-44e5-8a1f-a0b4bbebc936)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/1fc28285-c9fc-49b3-8df2-afb80eb04d75)

* Using the appropriate commands, we have the Fourier transform of the message signal and the modulated signal:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/9829980f-8762-41ec-91fd-543302e3f081)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/daaa96b9-54d2-4ddd-844b-fc8937d0b4a1)

<p align="justify"> As can be seen from the Fourier transform of the message signal, it has the general form of a sinc. For this reason, it is sinc because the message signal consists of pulses with different amplitudes. We know that the Fourier transform of the pulse signal is a sinc, for this reason, since the nature of our message signal is a pulse, then its Fourier transform is expected to be in the form of a sinc, which is also clear in the figure. For the Fourier transform of the modulated signal, it can be said that because it has been multiplied by a cosine term, and since the Fourier transform of the cosine is in the form of two pulses in its arc frequency, for this reason, the form of the Fourier transform of the modulated signal is two sinc shifts. The frequency of the carrier was 250 Hz, so for Fourier cosine conversion, we will have two pulses at 250 Hz and -250 Hz. As a result, by multiplying the message signal by this cosine term, the Fourier transform of the message signal (the same sinc in the first diagram) is shifted twice and at the mentioned frequencies is placed, which is also clear in the figure. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/2c9305fb-e748-413a-a791-b4fe954714e8)

* If the message signal is alternating with a period of $t_0$ , calculate the power and modulation efficiency for the modulated signal.

Modulated signal power:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/cebc9489-dedd-4c90-a0ed-9724f5c7751e)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/d9ebba09-fc24-4493-a307-5126f3144c3d)

Modulation efficiency:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/6d71ed48-be1b-49a8-9697-9798a6fbaf93)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/d7652149-36d7-463c-a7d7-f3e0c501b052)

* Using the "ammod" function, repeat the second request and explain how to use it for this question.

<p align="justify"> The arguments of this function are, respectively, the message signal (the amplitude of which is given as $A_c * \mu$ ), the carrier frequency, the sampling frequency, and the amplitude of the second term, which is $A_c$ . Using appropriate commands, we will have the modulated signal as shown below: </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/90e52a48-8fff-4274-bf8c-e88e9e2647fe)

## DSB and SSB Modulations
Assume the message signal to be as follows:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/48ce6b82-4f07-4416-8cc8-a48b563b80d1)

Sample the message signal in the range [-5,5] with a frequency of 600 Hz. 

* Plot the message signal in the time domain in seconds and its Fourier transform in Hz.

**Hint:** When sampling a continuous signal, the resulting signal is discontinuous. In the following relation, the relationship between the Fourier transforms of a continuous signal and its sampled signal in discrete time is stated, where $T_s$ is the sampling period, $\omega$ is the angular frequency of the discrete Fourier transform and $\Omega$ is the angular frequency of the continuous Fourier transform in terms of $[rad/s]$ . 

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/524a1368-b6e1-413b-899b-bb1c546428d7)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/7f06c170-f651-4996-8a8f-4ed304d78008)

<p align="justify"> Using the above relationships, we can see that for the signal amplitude, the scaling that takes place is that it must be multiplied by $T_s$ and for the frequency, the desired Fourier transform can be plotted with the above commands. The Fourier transform of the message signal is plotted in the following three frequency domains, and the last graph is actually the demand of the problem. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/9afbe1d5-b9da-45c3-b7de-916ba27e0182)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/7bd31f4b-429d-4328-bbdf-c67bd4dcf94b)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/69adde89-5dfe-4aeb-aac5-f0a077c11e67)

<p align="justify"> It should be noted that the shape of the Fourier transform of the message signal is triangular because the Fourier transform of the sinc is in the form of a pulse signal and the convolution of two pulses results in a triangular signal. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/42340987-39e4-4a99-8fd0-1d09b0066d40)

* <p align="justify"> Write a function that takes the message signal $m(t)$ , carrier wave amplitude $A_c$ and carrier wave frequency $f_c$ as input and returns the output resulting from the modulation 𝐷𝑆𝐵. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/9b9489cd-a729-4157-996f-26d03ea21662)

* <p align="justify"> Using the function of the previous section, modulate the message signal with frequencies $f_c$ = {50, 200} and plot the outputs. In another step, modulate the message signal with frequencies $f_c$ = {600, 1200} and plot the outputs. Determine the highest usable frequency of the carrier wave. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/4f1cc440-0055-460b-8592-8365c8e0ead9)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/09b305bd-eb4f-4067-84f1-fdb93ad961eb)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/1018e000-3a36-4ac4-a7c9-743355bb07db)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/80f8fee3-2ab5-4309-8662-8191c46182f5)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/e07fb62e-c82d-4910-a6b3-3ff0171ba58f)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/acc40192-c8bb-41f3-abdf-cf70b3a992d5)

<p align="justify"> According to the graphs, it is clear that in modulations with frequency of 50 and 200 Hz, the shape of the amplitude of the modulated signal almost matches the amplitude of the message signal and it can be identified. In fact, the frequency of 200Hz is better because the cosine signal that is placed inside it is more compact with a lower periodicity and makes the amplitude of the modulated signal more similar to the message signal. In two frequencies of 600 and 1200Hz, such explanations are not true. In fact, the main reason for this is that the Nyquist rate is not observed in these two frequencies and in this case the modulation is not done correctly. </p>

Now, in order to find the right range for $f_c$ , we must know that twice this frequency must be lower than the sampling frequency.

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/7d3cba1d-83ad-4ba3-8d28-382308fcbff7)

<p align="justify"> In addition to the above condition, the following inequality must also be satisfied to establish the Nyquist rate: ($f_N$ is the bandwidth frequency of the message signal). </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/507fa490-2251-4a1e-b994-1c8467fb1c20)

<p align="justify"> So, according to the above relations, in order to establish the Nyquist rate in order to modulate the signal in question and to correctly recover the message signal through the modulated signal, the carrier frequency must be higher than 60Hz and lower than 300Hz. In other words, the highest usable carrier wave frequency is 300Hz. In the first two graphs, this range is observed and we can see that the amplitude of the modulated signal is consistent with the message signal, but for the other two frequencies, 600 and 1200Hz, this is not true, and there is not even a trace of the cosine signal that is included in the message. This modulation mode is not done correctly. </p>

* Modulate the message signal with $f_c$ = 100Hz and $A_c$ = 1 and plot the Fourier transform of the output signal in Hz. 

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/a9b3aa2b-e903-42b1-b476-57aab712dbee)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/2fc3c74d-4cbd-4363-bdcf-d425fe6efb3e)

<p align="justify"> As it is clear from the diagrams, in the first diagram where the modulated signal is plotted, we can see that the amplitude of this signal has the approximate shape of the amplitude of the message signal, that is, the amplitude of the modulated signal is the amplitude of the function $sinc^{2}$ . Its maximum value is at zero time, which is 1, and in the negative part, we have the same value for the domain. For the Fourier transform of the modulated signal, it can be said that because during modulation, the DSB signal of the message is multiplied by a cosine term, and the Fourier transform of the cosine term includes two pulses at the frequencies of 100Hz and -100Hz, therefore, the form of the Fourier transform of the signal includes two The Fourier transform part of the message signal is shifted to 100 and -100 Hz frequencies. (Reminder: The Fourier transform of the function $sinc^{2}$ is a triangular signal, which can also be seen in the graph of shifted triangular signals. </p>

* <p align="justify"> Write a function that takes the modulated signal $x_{c}(t)$ , carrier wave amplitude $A_c$ and carrier wave frequency $f_c$ as inputs and extracts the message signal. To demodulate the message, you can use the diagram in the following figure. To apply the low-pass filter, you can Use the lowpass function. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/c804632c-d0f9-4296-8fe7-42d3eb1addb6)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/ca08c13f-479a-4cc8-a206-2eaa0fd2e007)

* <p align="justify"> Enter the modulated signal in the fourth section to the function of the previous section and set the other necessary parameters yourself. Then plot the signals $y(t)$ and $z(t)$, which are shown in the previous figure, in the time and frequency domain. The signal $z(t)$ is the output of the function you made in the previous section. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/dcf6585b-8643-4a48-a412-2417caa8e3ef)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/393e2b17-b920-49ca-aa20-85f3226977b0)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/a7cb207a-ad93-4c5b-9fd5-8e055fcebc4b)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/a1355a97-59df-4a59-8909-25048d4eadc8)

<p align="justify"> As it is clear from the figures above, the Fourier transform of the signal $y(t)$ is actually the product of the Fourier transform of the modulated signal and the Fourier transform of the cosine. The two triangular signals obtained in the fourth part are shifted to the frequencies of 100 and -100 Hz. In this shift, two of the triangular signals are placed at zero frequency, so the amplitude of the triangular signal that is at zero frequency is twice the other two triangular parts, which is also known in the figure. </p>

<p align="justify"> For the output signal of the function $z(t)$ it can be said that it has been correctly recovered because the signal of the initial message was also the same, and in the following these two signals are plotted together in the same graph. The Fourier transform of the signal $z(t)$ is also similar to the Fourier transform of the original message signal that we obtained in the first part. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/43ddaff6-3cf8-49c4-9f00-c6b4a14bf790)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/a27f615f-d50b-4867-9519-8ee26d1c54e3)

<p align="justify"> According to the diagram, we can see that the signal of the original message and the demodulated signal with the function we wrote are almost the same and the calculated error is very small. </p>

* <p align="justify"> Plot the graph of the error in the previous section with respect to the frequency of the carrier wave $f_c$ = [−500, 500 Hz] and determine the best value for the carrier frequency. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/415a268a-4849-42b8-bbc0-94a4375d7f3b)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/30acab38-ec53-482b-b1ce-d15eaa89cb92)

<p align="justify"> According to the diagram, the best ranges for the carrier frequency are actually the values ​​where the error diagram is minimal. That is, in the frequencies where we have the minimum value for the error, the demodulated signal is more consistent with the original message signal. So, according to the diagram, it can be said that in the following frequency range, the error value is minimal and the best modes are for the carrier frequency. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/be915d3b-53a3-409d-b904-9a99d2e0ec06)

* Results with "ammod" function:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/7ea92736-521a-4e5c-a5d2-27fa230578d1)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/693dfb8a-e18b-4a83-8b4d-f5b32410e1e7)

* Results with "amdemod" function:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/d0b60936-9226-4bc6-9f0c-cbbac8d5aec2)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/b967b571-13cb-4b02-ac71-1a6ee45d6f38)

<p align="justify"> As it is clear from the plotted figures, the output signals obtained from recovery or demodulation in this part and the sixth part have been unified. Their Fourier transform is also the same, and with a good approximation, it can be seen that their graphs are completely on top of each other. </p>

* <p align="justify"> Using the "ssbmod" function, the message signal with $f_c$ = 100Hz and $A_c$ = 1 is lower-sideband and modulate the upper sideband and plot the Fourier transform of the output signal in Hz. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/9da84180-9f2c-4b1a-8003-01f0f7972621)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/bc6f25ea-e950-44ae-b278-a6e714f9a9bc)

<p align="justify"> As we expected in the figures, in the LSB mode, the Fourier transform part should be seen at low frequencies, and in USB, the Fourier transform should be seen with high frequencies. The Fourier transform of the modulated signal was in the form of two triangular signals at the frequencies of 100 and -100 Hz (the same as the carrier frequency), so according to the figure, the low frequencies should be in the first diagram and the high frequencies should be in the second diagram. </p>

## Hilbert Transform and Envelope Detector
* The Hilbert transform relation in the discrete domain is as follows:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/7a74b5b2-0f91-4cc6-8a7a-fab8b70b0646)

The relation we have for the Hilbert transform in the continuous domain is as follows:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/12b04854-d6bd-494e-bca3-b15815897d12)

For the time domain, the discrete Hilbert transform is as follows:

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/155a0e72-7718-41c1-a743-e68b78aed1ec)

* The periodic message signal is defined as follows. Find its Hilbert transform using the "hilbert" function.

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/594dabaf-8cc9-4c70-9810-492606da0ba5)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/d34d54f1-a86a-4315-9a25-34f4e83735b3)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/5bcb4d3c-d739-4f22-b3b5-83c3898f22e1)

* <p align="justify"> Using the appropriate frequency that you determined in the second part, modulate this message as 𝐷𝑆𝐵 with carrier signal amplitude equal to 1 and plot it in the time domain. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/9ff19ed4-b2ca-435b-af1c-6ade81f04476)

* Recover the message signal using the envelope detector (obtained by Hilbert transform).

<p align="justify"> According to the graphs we plotted above, if we plot the size of the Hilbert transform of the modulated signal in the form of DSB, we can see that the same signal as the original message is revealed. So, in this domain detection method, the signal of the original message can be recovered with a relatively good approximation. </p>

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/1aa18c1b-dc7a-4246-a8bb-cf3c74648672)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/852c22c6-0940-4a71-a17f-227837b8cbe1)

![image](https://github.com/SogolGoodarzi/AM-DSB-SSB-Modulations/assets/125180530/3e4fa40b-b273-48f0-bb6a-c04be1f7442d)
