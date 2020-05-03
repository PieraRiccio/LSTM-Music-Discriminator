## Music Discriminator with LSTMs

 * Discriminate music as being composed by humans or by a generative model.
 * Use multiple layers of LSTM Recurrent Neural Nets
 * Implementations in PyTorch and Keras.

### Test trained LSTM model
 In the `./weights/` you can find trained model weights and model architecture.

 To test the model on your custom audio file, run

     python3 predict_example.py path/to/custom/file.mp3
 or to test the model on our custom files, run

     python3 predict_example.py audio/classical_music.mp3

### Audio features extracted
 * [MFCC](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum)
 * [Spectral Centroid](https://en.wikipedia.org/wiki/Spectral_centroid)
 * [Chroma](http://labrosa.ee.columbia.edu/matlab/chroma-ansyn/)
 * [Spectral Contrast](http://ieeexplore.ieee.org/document/1035731/)

### Dependencies
 * [Python3](https://www.anaconda.com/distribution/#download-section)
 * [numpy](https://numpy.org)
 * [librosa](https://librosa.github.io/librosa) &rarr; for audio feature extraction
 * [Keras](https://keras.io)
    * `pip install keras`
 * [PyTorch](http://pytorch.org)
    * `pip install torch torchvision`
    * `brew install libomp` 

### Ideas for improving accuracy:
 * Normalize MFCCs & other input features ([Recurrent BatchNorm](https://arxiv.org/pdf/1603.09025v4.pdf)?)
 * Decay learning rate
 * How are we initing the weights?
 * Better optimization hyperparameters (too little dropout)
 * Do you have avoidable bias? How's your variance?
