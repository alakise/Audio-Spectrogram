
# Audio-Spectrogram
Generating sound spectrograms using short-time Fourier transform that can be used for purposes such as sound classification by machine learning algorithms.

You can read more about the code repository in the following article: 
[Creating Spectrograms From Audio Files Using Python](https://www.alakise.com/bilgisayar-bilimi/makine-ogrenimi/creating-spectrograms-from-audio-files-using-python).

Also available in Turkish:
[Python ile Ses Dosyalarının Spektrogramlarının Oluşturulması](https://www.alakise.com/bilgisayar-bilimi/makine-ogrenimi/python-ile-ses-dosyalarinin-spektrogramlarinin-olusturulmasi/)
 ## Compatibility
The code is tested using SciPy 1.3.1, NumPy 1.17.0, Matplotlib 3.1.1 under Windows 10 with Python 3.7 and Python 3.5. Similiar versions of those libraries probably works.
 
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
## How to contribute
I encourage you to share the code that you use for audio processing and analysis. Sharing code helps to make studies reproducible and promotes collaborative research. To contribute, please:

-   Fork the repository using the following link:  [https://github.com/alakise/Audio-Spectrogram/fork](https://github.com/alakise/Audio-Spectrogram/fork).
-   Commit your changes to the forked repository.
-   Submit a pull request to  [this repository](https://github.com/alakise/Audio-Spectrogram/)
## License

By committing your code to the this repository  you agree to release the code under the MIT License attached to the repository.
