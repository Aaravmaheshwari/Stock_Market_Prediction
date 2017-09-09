# Stock Market Prediction


# Coding Challenge - Due Date, Thursday Sept 14 12 PM PST

Train a machine learning model of your choice on a company stock's historical data as well as 3 other data points. They can be the sentiment from twitter, news headlines, google trends, etc. Be creative, good luck!

## Overview

I wanted to use DeepMind's [WaveNet](https://deepmind.com/blog/wavenet-generative-model-raw-audio/), as it's meant for time series analysis and brings us awesome results for audio/TTS/music generation. I wanted to bring this technique outside of audio analysis, in this case to the stock market.

We need to have a local conditioning available to be able to cope with changing constraints, which is to my knowledge only available inside this repository:
https://github.com/dannybtran/tensorflow-wavenet

As it expects audio input, I will just write the stock price data into a wav file and put it into the wavenet.

## Results

## Credits

Thanks dannybtran for the implementation of local conditioning
Thanks ibab for implementing wavenet in tensorflow
Thanks DeepMind for WaveNet