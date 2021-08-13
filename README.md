# Video-Captioning-Implementations
Automatically generate natural language sentence based on the content of the short video clips.

## Goal
- Understand Encoder-Decoder architecture.
- Use the architecture in the paper as a reference to reproduce our own version in PyTorch.

## Model
Developed 2 CNN-RNN architectures for video caption generator.
CNN architectures are used for visual encoding and RNN structures are used for decoding.
1. Fixed Representational Context

![](sample/model1.png?raw=true)

2. Sequence to Sequence

![](sample/model2.png?raw=true)

## Sample result on testing data

| Video | Text (Greedy)|
|-------|----------|
|![](sample/F2Ny7rq9RKs_139_148.avi.gif?raw=true)|“a person is adding ingredients into a bowl”
|
|![](sample/r2oI9Y-3wAo_21_28.avi.gif?raw=true)|“a panda bears is climbing up a bench”|

## Other technical details

- Generated visual encoding vectors from each video using resnet50 or VGG16

- Used google-news-300 word2vec for language encoding

- Used Teacher Forcing Ratio for training RNN



## Future Development
- Add attention layers                          
- Implement dense video captioning
- Beam search for text generation
- Add BLEU Score

## References
S. Venugopalan et al. 2015. Sequence to Sequence - Video to text. In IEEE ICCV<br>
S. Venugopalan et al. 2014. Translating videos to natural language using deep recurrent neural networks. arXiv preprint arXiv:1412.4729.<br>
Neyyer Aafaq et al. 2020. Video Description: A Survey of Methods, Datasets and Evaluation Metrics. arXiv preprint arXiv:1806.00186v4.
