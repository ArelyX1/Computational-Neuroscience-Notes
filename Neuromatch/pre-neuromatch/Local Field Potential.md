We have multiple electrical measurements of brain activity like a:
- **Single-Unit and Multi-Unit Activity (SUA / MUA):** Extracellular detection of individual or small-group action potentials (_spikes_) using microelectrodes
- Electrocorticography (ECoG / intracranial EEG): Invasive recording of cortical field potentials using electrode arrays placed directly on the cerebral surface.
- Electroencephalography (EEG): Non-invasive recording of macroscopic cortical electrical activity measured from the scalp.



But in this time we will talk about LFP,  in summary, that record the signals.

Recorded signal split into 2 frequency bands:
- High frequency >500 Hz : Multi Unit Activity MUA
- Low frequency < 300 Hz: Local Field Potential -> measures subthreshold activity due to synaptic inputs from **populations** of neurons
LFP it subject, that have no context so with that haven't some analysis of the brain activity

![[Pasted image 20261107142120.png|471]]

Exists a formula to know the link between brain activity and these extracellular recorded potentials -> goes via transmembrane current of the neurons. So when simulate a neuron activity, you simulate in thee membrane potential in the soma because that's where it's sort of decided whether this neuron generates an action potential or not.

Biophysical forward-modeling formula
$$
\phi(r, t) = \frac{1}{4\pi\sigma} \sum_{n=1}^{N}\frac{I_{n}(t)}{|r-r_n|}
$$
![[Pasted image 20261107143905.png]]

# Example LFP from pyramidal neuron model

![[Pasted image 20261107144038.png]]

![[Pasted image 20261107144728.png]]