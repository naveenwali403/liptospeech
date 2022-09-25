# liptospeech

There is different ways to tackle this problem (sorted from the lowest to the highest level of abstraction) :

Lip reading on the phoneme level: For every frame of the input, predict the corresponding phoneme. The classification problem is easier (only 44 different phonemes in English), but going up to a higher level to form words or sentences can be challenging : (1) a phoneme can be spread over multiple frames, (2) and some phonemes are impossible to differentiate (from a lip movement perspective, there is no way to distinguish between and “p” and a “b” for example).
Lip reading on the word level: Parse the video sequence into different subsequences with each one of them containing a single word. Then classify those sequences using a predefined dictionary. This classification problem is more difficult, given that the dictionary should contain a lot of words (>100). But also because we first need to parse the input into different subsequences.
Lip reading on the sentence level: Predict words in a sentence using predefined phrasing. Not really useful in my own opinion.
Here I chose to work on the word level because even if a high accuracy is not achieved, the output can still be used to enhance speech recognition models.

Possible applications
For humans, adding sight of the speaker to heard speeches improves speech processing. In the same way, a lip reading AI can be used to enhance some already existing speech recognition models, especially if the audio is noisy (low quality, music in the background, etc.)
