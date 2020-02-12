# Speech_Recognition_with_Tensorflow
Implementation of a seq2seq model for speech recognition. Architecture similar to "Listen, Attend and Spell".
https://arxiv.org/pdf/1508.01211.pdf

![alt text](https://github.com/thomasschmied/Speech_Recognition_with_Tensorflow/blob/master/imgs/seventeen_twenty_four.png)
```
Created: ['S', 'E', 'V', 'E', 'N', 'T', 'E', 'E', 'N', '<SPACE>', 'T', 'W', 'E', 'N', 'T', 'Y', '<SPACE>', 'F', 'O', 'U', 'R']
Actual: ['S', 'E', 'V', 'E', 'N', 'T', 'E', 'E', 'N', '<SPACE>', 'T', 'W', 'E', 'N', 'T', 'Y', '<SPACE>', 'F', 'O', 'U', 'R']
```



## Prerequisites
- Tensorflow
- numpy
- pandas 
- librosa
- python_speech_features

## Datasets
The dataset I used is the LibriSpeech dataset. It contains about 1000 hours of 16kHz read English speech.
It is available here: http://www.openslr.org/12/

## Code 
I uploaded three **.py** files and one **.ipynb** file. The .py files contain the network implementation and utilities. The Jupyter Notebook is a demo of how to apply the model.

## Architecture
**Seq2Seq model**\
As I mentioned above the model architecture is similar to the one used in "Listen, Attend and Spell", i.e. we are using pyramidal bidirectional LSTMs in the encoder. This reduces the time resolution and enhances the performance on longer sequences.

- Encoder-Decoder
- Pyramidal Bidirectional LSTM
- Bahdanau Attention
- Adam Optimizer
- exponential or cyclic learning rate
- Beam Search or Greedy Decoding
