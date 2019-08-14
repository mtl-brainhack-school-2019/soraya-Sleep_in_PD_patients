# Predict Apnea-Hypopnoea index (AHI) in Parkinson's patients with obstructive sleep apnea #
Obstructive sleep apnea (OSA) can be common in patients with Parkinson's disease (PD); it is thought that PD, through weakened muscle and autonomic dysfuntion, can lead to OSA. A marker of autonomic dysfunction often looked at is heart rate variability (HRV); I plan on computing this variable from sleep data and then use this variable to predict (probably through a linear regression) the severity of obstructive sleep apnea in the sample of patients I have. I have sleep recordings from ~20 PD patients, ranging in OSA severity.

# List of things to do: #
- [ ] Remove artifacts from sleep recording (visbrain sleep ?)
- [ ] Compute HRV with python:
    - [ ] Process the signal and divide low frequency band and high frequency band
- [ ] Try diff supervised algorithms and see which best match the variable (is the relationship linear or not? is there even a relationship...)

- [ ] I also want to make some nice visualizations; topo maps across sleep stages of EEG activity (frontal, central, occipital) with apnea episodes

## Some issues/Questions i have for myself: ##
- I have many hours of recording (~7hours), where do I sample my signal from? Do I average the whole 7 hours? What about different sleep stages??? Do i sample diff time points (early night, mid night, late night)

I also want to look at more...brain data, but because of the time constraint i am not sure if that is possible (noisy signal and not a lot of active electrodes). 

### Some references and info for myself ###
    refs: 
    https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4083342/
    https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5437978/
    https://link.springer.com/article/10.1007%2Fs11325-018-1729-0

To calculate HR variability, need to compute diff freq bands of ECG:
"Frequency bands were divided into very low frequency (0.003 to 0.04 Hz), low frequency (0.04 to 0.15 Hz), and high frequency (0.15 to 0.4 Hz) categories. The frequency domain parameters were VLF [%], LF [%], HF [%], LF/HF, LF [n.u.], HF [n.u.], VLF [abs], LF [abs], and HF [abs]." (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4890801/)