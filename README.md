# PBCH SSB



PBCH
It carries the broadcast information known to be as MIS (minimum system information). It carries information like SSB index, half-frame number and system frame number. It is also used for frame and slot synchronization. Now, the modulation used for PBCH is QPSK modulation and it also has the DMRS signals used to know the condition of PBCH or the condition of the PBCH channel. It carries its own frequency-multiplexed DMRS and in this, the polar coding is used. 


SSB 
It consists of SSS, PSS and PBCH. In the time domain, it occupies the SS or PBCH block consisting of four OFDM symbols (values 0-3). It is broadcast periodically by using the beamforming technique. While performing the UE cell search procedure, the decoding of the SS block is the first step. 


PBCH Structure
If we talk about the position of DMRS, then it is one out of four of every resource block. Let's say we have 20 resource blocks out of which let's say we select the third symbol. Now the third symbol will have 12 subcarriers starting from 0 to 11. Now, the one block is carrying the PBCH information and the second different block contains the DMRS. Now if you want to calculate the position of DMRS, it can be done by using the formula DMRS offset = NcellID mode4, which means that every 4th resource block is going to be our PBCH DMRS in that particular symbol. 


DMRS (Demodulation Reference Signal)
There are almost eight possible DMRS sequence data that are tried by the device or UE. If one particular sequence has the maximum SINR estimation then that will be kept by the UE or device. As we discussed previously, polar coding is used. That polar coding has 32 bits of information. In which, the RRC produced 24 bits and the Layer-1 generates the 8 bits of timing information. For frequency range-2 it contains 3 MSB of the SSSB index. 


SSB transmission pattern in the time domain 
It depends on the configured subcarriers and frequency band deployment. The subcarrier here can be taken at 15 kHz, 30 kHz, 60 kHz, 120KHz or 240 kHz. And the representation of the position of symbols is done by using the formula, {2,8} + 14n for 15KHz. Now, if the frequency is less than 3 GHz then the "n" used in the position of the symbol formula will be (0,1) and if a frequency is between 3GHz to 6GHz then the "n" will be (0,1,2,3). 
Let us take the example of 30 kilohertz. So in that case, the formula used will be {4, 8, 16, 20} + 28n. Here, "n" is (0,1). If we take n as 0 and put this in that formula then, the position of the OFDM symbol is (4, 8, 16, 20). 
There is a SS block which it includes 4 symbols and these symbols are carrying information about the PSS and SSS. So 4 to 8 is one SS block and 8 to 12 is another SS block. And these two blocks combine to have SSB Burst. So, if we take a 30 kHz example with n=0,1 then the SSB burst is 4.
 


SSB Burst
It is basically the set of consecutive SS blocks. In 5G, if the frequency is less than 6GHz then there is 2 SS block and if the frequency is greater than 6 GHz then there is 4 SS block in a single burst.


SSB Burst Set 
It comprises multiple SSB bursts or we can say it defines a maximum number of SSB in a particular burst set. If the frequency is up to 3 GHz, then the maximum number of SSB in one burst set is 4. If the frequency is between 3 to 6 GHz, then the maximum number of SSB in one burst is 8. And if the frequency is between 6 to 52.6 GHz then the maximum number of SSB in one burst is 64.
