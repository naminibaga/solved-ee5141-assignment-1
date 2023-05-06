Download Link: https://assignmentchef.com/product/solved-ee5141-assignment-1
<br>
<ol>

 <li>Jakes’ Model : This is a deterministic, time domain model for effective fading channelsimulation.</li>

</ol>

The fading waveform is modeled using <em>M </em>+ 1 oscillators.The oscillator frequencies are given by <em>f<sub>n </sub></em>= <em>f<sub>d </sub></em>cos(2<em>πn/N</em>) for <em>n </em>= 1<em>,</em>2<em>,</em>3<em>,…….M</em>, where <em>N </em>= 4<em>M </em>+ 2 and <em>f<sub>d </sub></em>is the maximum doppler frequency. The expression for the fading model is given by

where <em>β<sub>n </sub></em>= <em>πn/</em>(<em>M</em>+1) and <em>φ<sub>n </sub></em>are uniformly distributed between [−<em>π,π</em>). The simulation programme must accept two inputs (Doppler frequency <em>f<sub>d </sub></em>and duration of fading waveform in seconds). The fading waveform must be sampled at a rate of at least 1000 samples/sec, and the average received envelope should be 0 dB (normalization).

<ul>

 <li>Write simulation code to generate Rayleigh fading by Jakes’ method. Provide plotof received envelope <em>v </em>(in dB) versus time for <em>f<sub>d </sub></em>= 1 Hz<em>, </em>10 Hz and 100 Hz, for a duration of 1 second. Use <em>M </em>= 20.</li>

</ul>

1

<ul>

 <li>Generate fading <em>f<sub>d </sub></em>= 100Hz for 5 seconds using Jakes’ method. Compute the normalized level crossing rate versus(dB). Consider <em>ρ </em>in the range</li>

</ul>

(−22 dB, 5 dB) in steps of 3 dB. Average the values by repeating the experiment. Plot the measured level crossing rate. On the same plot, show the theoretical level crossing rate for the entire range of <em>ρ</em>.

<ul>

 <li>Generate fading <em>f<sub>d </sub></em>= 10 Hz for 5 seconds using Jakes’ method. Compute the normalized duration of fade (¯<em>τf<sub>d</sub></em>) versus <em>ρ </em>(dB). Consider <em>ρ </em>in the range (−22 dB, 5 dB) in steps of 3 dB. Average the values by repeating the experiment. Plot the measured value of the average duration of fade. On the same plot, show the theoretical graph for the normalized duration of fades for the entire range of <em>ρ</em>.</li>

 <li>Modify the Jakes’ model to generate Ricean fading for <em>k </em>= 1<em>,</em>4<em>, </em>and 10 (<em>f<sub>d </sub></em>= 100 Hz and <em>t </em>= 1 sec). Plot the figures along with the Rayleigh fading signal. Record your observations.</li>

</ul>

<ol start="2">

 <li>Clarke’s Model (Frequency Domain):[Refer Wireless Communication, Theodore S. Rappaport Second Edition, Section 5<em>.</em>7<em>.</em>2] The following steps are required for simulation:</li>

</ol>

<ul>

 <li>Specify the number of frequency domain points (<em>N</em>) used to represent <sup>p</sup><em>S<sub>E</sub></em><em><sub>z</sub></em>(<em>f</em>) and the maximum doppler frequency shift be <em>f<sub>d</sub></em>. The value of <em>N </em>is usually a power of</li>

</ul>

two. .

<ul>

 <li>Compute the frequency spacing between adjacent spectral lines as ∆.</li>

</ul>

This defines the time duration of the fading waveform, <em>T </em>= 1<em>/</em>∆<em>f</em>.

<ul>

 <li>Generate complex Gaussian random variables for each of the <em>N/</em>2 positive frequency components of the noise source.</li>

 <li>Construct the negative frequency components of the noise source by conjugating thepositive frequency values and assigning these at negative frequency values.</li>

 <li>Multiply the in-phase and quadrature noise sources by the fading spectrum <sup>p</sup><em>S<sub>E</sub></em><em><sub>z</sub></em>(<em>f</em>).</li>

 <li>Perform IFFT on the resulting frequency domain signals from the in-phase and quadrature arms to get two <em>N</em>-length time series , and add the squares of each signal point in time to create an <em>N </em>point time series.</li>

 <li>Take the square root of the sum obtained in step (f) to obtain an <em>N</em>-point time series of a simulated Rayleigh fading signal with the proper Doppler spread and time correlation.</li>

</ul>

Assume <em>f<sub>d </sub></em>to be 10Hz. Generate 50 sample functions of fading data set. Using the observed data to find <em>N<sub>v </sub></em>and ¯<em>τ </em>for <em>ρ </em>= 1<em>,</em>0<em>.</em>1<em>,</em>0<em>.</em>01. Compare these values with the theoretical values. Repeat the process for <em>f<sub>d </sub></em>= 100 Hz.

2