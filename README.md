# spectroFROG

Artificial neural network (ANN) is used to classify frequency resolved optical gating (FROG) spectrograms based on the phase
of the corresponding pulse.

Generally, ultrafast spectroscopy requires a short pulse. When the different frequencies that consitute the pulse grow out of
phase, the pulse grows longer and the time resolution of the spectroscopic measurement becomes longer. The pulse can be 
represented in the time domain or the frequency domain. The time domain shows us how short the pulse is and the frequency
domain shows us if the different frequencies are in phase. A short, compressed pulse is shown below:

![alt text](https://github.com/pbrosseau/spectroFROG/blob/main/spectroFROG_pulse_compressed.png?raw=true)

while an un-compressed pulse is shown here:

![alt text](https://github.com/pbrosseau/spectroFROG/blob/main/spectroFROG_pulse_uncompressed.png?raw=true)

The goal of pulse compression is to manipulate the phase of the uncompressed pulse until it resembles a compressed pulse.
This can be achieved with a pulse shaper, such as an acousto-optic programmable dispserive filter (AOPDF). An AOPDF can
apply a phase mask to correct the phase of an un-compressed pulse. The Dazzler AOPDF, by Fastlite, applies a fourth-order
polynomial to the pulse phase. One then desirese to know what fourth-order polynomial best compresses a given pulse.

Frequency resolved optical gating (FROG) is a pulse characterization method that generates a spectrogram (x-axis: time, 
y-axis: frequency) that is defined by a given input pulse. The FROG corresponding a compressed pulse appears vertical,
as there is no relative delay between frequencies:

![alt text](https://github.com/pbrosseau/spectroFROG/blob/main/spectroFROG_pulse_compressed_FROG.png?raw=true)

However, the FROG from the un-compressed pulse is broader and has a characteristic shape that is defined by its spectral
frequency:

![alt text](https://github.com/pbrosseau/spectroFROG/blob/main/spectroFROG_pulse_uncompressed_FROG.png?raw=true)
