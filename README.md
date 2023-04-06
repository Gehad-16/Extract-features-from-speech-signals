# Extract-features-from-speech-signals
Extract features from speech signals

- Any signal can be classified as being either stationary or non-stationary. Speech signals are known to be quasi stationary, i.e. stationary for very short periods of time (10-20 msec, which is the usual frame size that will be used in our program).
- Does the 10-20 msec represent the time of a sentence, word or phoneme? Does it make sense that the properties of a signal are stationary throughout a sentence, word or phoneme? Usually people will believe that the 10-20 msec are the timing of a phoneme. However, the properties of a phoneme differ based on what phoneme precedes it and what phoneme succeeds it, i.e. phonemes are not pronounced in isolation.


- They are co-articulated based on the context in which they exist. Hence, the 10-20 msec, is a time period less than the period of a phoneme, were the properties of a speech signal are usually constant. 
- Hence, from now on, before processing a speech signal, we divide it into frames of size 10-20 msec, and any processing is done on each frame separately, i.e. preprocessing, feature extraction, pitch period extraction, etc. are all performed on each frame separately.
- However, if we take for instance the first frame from 0-10 msec, and the second frame from 10-20 msec, any properties on the boundary between the 2 frames will be lost. 


- Hence, to avoid loss of information/ properties, we usually overlap frames to ensure continuity. 
- The percentage of the frame that overlaps with its preceding frame is called “frame overlap”. 
- The percentage of frame size that is not common between consecutive frames is called “frame spacing” or “frame shift”. 
- If the amount of frame overlap is x % of the frame size, then the amount of frame spacing/ shift is (1-x)% of the frame size.
- However, if the frame overlap is defined in terms of milliseconds (e.g. 5 msec), and the frame size is known (e.g. 20 msec), then the frame shift/spacing is 15 msec (20 msec-5 msec).


- Performing framing is like multiplying the speech signal by a rectangular window of size 10-20 msec. 
- Multiplying in time domain is equivalent to convolution in the frequency domain. 
- Hence, it is as if the original signals frequency representation is convoluted with the sinc function (rectangular window in the time domain, is a sinc function in the frequency domain), which will distort the signals frequency representation to some degree due to the ripples in the sinc function.
- The ripples are a result of the sharp fall off at the edge of the rectangular window. 
-  Hence to solve this problem after getting the frames, we can multiply each frame by hamming, hanning or any other window type (of the same size as the frame). Such windows have much less ripples in their frequency representation due to their smooth edges in the time domain.
