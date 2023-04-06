# Extract-features-from-speech-signals
Extract features from speech signals

**The program is divides any input speech signal into frames. The user can specify any frame size, any overlap size and any window type.**

## Inputs: 

1. Audio File Path
2. Frame size in seconds
3. Overlap size in seconds
4. Window type to be used

## Outputs:

1. Matrix containing frames (one frame per row)
2. Plot of original signal.
3. Plot of framed signal. This is to ensure that you have framed correctly. If you choose a certain frame size and an overlap size of 50% of the frame size, the framed signal’s plot will be almost twice the length of the original signal’s plot.

## Program Summary:
- We use the “wavread” function to read the audio file into a vector, as well as the sampling rate. Then, the frame size and overlap size (in seconds) can be converted into samples. In other words, 
- •	Frame size (samples) = frame size (seconds) * Sampling Rate (samples/second)
- •	Overlap size (samples) = Overlap size (seconds) * Sampling Rate (samples/second)
- Then we can iterate on the vector containing the data, and extract samples equivalent to the frame size in samples and with overlap equivalent to overlap size in samples. 
- Such frames are placed in a new matrix, where each row corresponds to a frame.
-  If the user chose a rectangular window, then the previous matrix is the final one. Else, if the user chose a hamming or hanning window, then the student should construct a hamming/hanning window of the same size as the frame size, and multiply each row of the frames matrix by this window. The student should then plot the original and the framed signal. 




