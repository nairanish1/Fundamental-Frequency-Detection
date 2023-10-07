# Pitch Tracking with Autocorrelation Function (ACF)
## Overview
This repository contains a Python-based audio analysis system that estimates the pitch (fundamental frequency) of an audio signal using the Autocorrelation Function (ACF). The objective is to provide an intuitive pitch tracking mechanism for audio signals and evaluate its efficacy against known fundamental frequencies.

## Key Features
### Block Audio Processing: 
Splits the audio signal into overlapping blocks to facilitate block-wise processing.
### ACF Computation: 
Computes the autocorrelation of an audio signal.
### Pitch Estimation: 
Estimates the fundamental frequency using the computed ACF.
### MIDI Conversion: 
Converts the estimated frequencies to MIDI notes.
### Error Evaluation:
Compares the estimated frequencies with ground truth to compute RMS error in cents.
### Test Signal Generation: 
Generates test sinusoidal signals of specified frequencies.
### Plotting Mechanism:
Visualizes the estimated frequency and error over time.
### Bulk Evaluation:
Evaluates the performance of the pitch tracker on a directory of .wav files and their corresponding ground truth data.
Instructions
## Prerequisites:
Ensure you have numpy, scipy, and matplotlib installed.
## Running the Code:
Use the generate_sine() function to create a test sinusoidal signal. Parameters include freq1, freq2, amp, dur, and fs.
To visualize the estimated pitch and the corresponding error of a test signal, call the plot_test() function after generating the test signal.
For bulk evaluation on a directory of .wav files, use the run_evaluation() function. It requires the complete path to the data folder containing .wav files and their corresponding .f0.Corrected.txt files for ground truth.
## Technical Details
block_audio(): Splits the audio signal into overlapping blocks.
comp_acf(): Computes the autocorrelation of an audio block.
get_f0_from_acf(): Estimates the fundamental frequency of a block using its ACF.
track_pitch_acf(): Estimates the pitch of an entire audio signal using ACF.
convert_freq2midi(): Converts a frequency in Hertz to a MIDI note number.
eval_pitchtrack(): Compares estimated frequencies with ground truth and returns RMS error in cents.
generate_sine(): Generates sinusoidal signals of two specified frequencies.
plot_test(): Plots the estimated frequencies and the RMS error for a test signal.
run_evaluation(): Evaluates the system's performance on a directory of .wav files.
## Notes
The algorithm is sensitive to the configured min and max lag values. While it performs well when the fundamental frequency range is known, results can be unpredictable on more generalized signals.
While the ACF method offers a straightforward approach to pitch tracking, it may not always be the most robust, especially in the presence of noise or harmonic complexity.
Developed by:

Brittney
Jerry
Anish B1.
Anish and Jerry B2.
Feedback, contributions, and issues are welcome.
