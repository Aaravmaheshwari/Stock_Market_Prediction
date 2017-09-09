# Stock Market Prediction


# Coding Challenge - Due Date, Thursday Sept 14 12 PM PST

I tried to predict the MSFT stock price, using S&P 500 index (kind of a baseline stock market movement), the GDP of the last year ("how much are people able to afford?") and the mean temperature on the trading day ("how did the traders feel on that day?").

## Overview

I wanted to use DeepMind's [WaveNet](https://deepmind.com/blog/wavenet-generative-model-raw-audio/), as it's meant for time series analysis and brings us awesome results for audio/TTS/music generation. I wanted to bring this technique outside of audio analysis, in this case to the stock market.

We need to have a local conditioning available to be able to cope with changing constraints, which is to my knowledge only available inside this repository and not well tested:
https://github.com/dannybtran/tensorflow-wavenet

As it expects audio input, I will just write the stock price data into a wav file and put it into the wavenet.

It didnt work very well using the actual value, as it's almost the same all the time (even if scaled), so I tried using the daily change in percent as input.

## Results
![res](https://github.com/hutauf/Stock_Market_Prediction/blob/master/result.png)

As we can see, MSFT should have crashed according to wavenet :)
It seems like it really likes the -3% daily chance.

## Credits

Thanks dannybtran for the implementation of local conditioning

Thanks ibab for implementing wavenet in tensorflow

Thanks DeepMind for WaveNet