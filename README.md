
# Audio-Spectrogram
Generating sound spectrograms using short-time Fourier transform that can be used for purposes such as sound classification by machine learning algorithms.

## Background
I needed an audio spectrogram generator for a machine learning algorithm I wanted to produce, but all the codes I encountered were missing, old or incorrect.

The problem I encountered in all the codes, the output of the code they wrote was always at a standard resolution. I’ve arranged the output resolution to be equal to the maximum resolution that the audio file can provide, making it the best fit for analysis(not sure). I also standardized the expression of sound intensity as dBFS.
### Theory
Audio files are actually records of periodic sampling of the sound levels of frequencies. I want to touch on these notions first.

### Sound Level
Differences in signal or sound levels are measured in decibels (dB). So a measurement of 10 dB means that one signal or sound is 10 decibels louder than another. It is a relative scale.

It is a common error to say that, for instance, the sound level of a human speech is 50-60 dB.  The level of the human speech is 50-60 dB SPL(Sound Pressure Level), where 0 dB SPL is the reference level. 0 dB SPL is the hearing limit of average person, anything quieter would be imperceptible. But dB SPL relates only to actual sound, not to signals.

I’ve scaled plot to dbFS, FS stands for ‘Full Scale’ and 0 dBFS is the highest signal level achievable in a digital audio file and all levels in audio files relative to this value.

### Frequency
Audio frequency is the speed of the sound’s vibration which determines the pitch of the sound. Even if you are not familiar with audio processing, this notion widely known.

### Sampling Rate
The sampling rate is the number of times per second that the amplitude of the signal is measured and so has dimensions of samples per second. So, if you divide the total number of samples in the audio file by the sampling rate of the file, you will find the total duration of the audio file. For further information about sampling rate search for “Nyquist-Shannon Sampling Theorem”

Fourier Transform and Short Time Fourier Transform
If we evaluate a sound wave as a time-volume graph, we cannot obtain information about the frequency domain, and if we apply a Fourier transform to this wave, it loses its time domain. In short, time represention obfuscates frequency and frequency represention obfuscates time. Therefore, a meaningful image in terms of frequency, sound intensity and time can be obtained by applying the Fourier transform to the short interval parts of the sound data called short time Fourier transform.

 ## Compatibility
The code is tested using SciPy 1.3.1, NumPy 1.17.0, Matplotlib 3.1.1 under Windows 10 with Python 3.7 and Python 3.5. Similiar versions of those libraries probably works.
Only supports mono 16bit 44.1kHz .wav files. But it is easy to convert audio files using certain websites.

 ## Usage
You can run the code on the command line using:

    python spectrogram.py "examples/1kHz-20dbFS.wav" l # opens labelled output in window
    python spectrogram.py "examples/1kHz-20dbFS.wav" ls # saves labelled
    python spectrogram.py "examples/1kHz-20dbFS.wav" s # saves unlabelled output
    python spectrogram.py "examples/1kHz-20dbFS.wav"  # opens unlabelled output in window

The third argument passed on the command line can take two letters: 'l' for labelled, and 's' for save. Set your output folder in code.

Example labelled output in window (1kHz-20dbFS.wav - 1kHZ sinus wave at -20dBFS):
![1kHz sinus wave at 20dbFS for 3 seconds.](https://www.alakise.com/wp-content/uploads/2019/08/image-5.png)



## Test
Tested with audio files in "examples" folder. Following images shows two of them:
1kHz-10kHz Sweep -40dbFS:
![](https://www.alakise.com/wp-content/uploads/2019/08/image-6-1024x586.png)

Me saying "Merhaba Dünya"(hello world):
![](https://www.alakise.com/wp-content/uploads/2019/08/image-7.png)

## License

By committing your code to the this repository  you agree to release the code under the MIT License attached to the repository.
