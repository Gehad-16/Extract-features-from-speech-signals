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

## sample of output:
![image](https://user-images.githubusercontent.com/63863517/230358667-1cdfab89-96fe-47bc-aba7-559e061d6bf4.png)
![image](https://user-images.githubusercontent.com/63863517/230359189-ac058a3f-4a49-4f24-ab09-14a64ffcdb4e.png)
![image](https://user-images.githubusercontent.com/63863517/230359244-fb28d02f-915a-4a17-89b7-c27868e39c53.png)
![image](https://user-images.githubusercontent.com/63863517/230359340-59bf4d68-f6b8-4f76-a49d-8cff1eb3f88c.png)
![image](https://user-images.githubusercontent.com/63863517/230359406-eab7f5b7-8655-4fbb-9ec3-859dddfbe788.png)
![image](https://user-images.githubusercontent.com/63863517/230359529-d11069ae-101d-418d-9623-9ea04f8a106b.png)![image](https://user-images.githubusercontent.com/63863517/230359616-d6a908f2-0631-414d-8531-605287c6233d.png)







