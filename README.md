# Video-Captioning-Implementations
Automatically generate natural language sentence based on the content of the short video clips.

## Goal
- Understand Encoder-Decoder architecture.
- Use the architecture in the paper as a reference to reproduce our own version in PyTorch.

## Daset
Microsoft Research Video Description Corpus (MSVD) [1] and Microsoft Research Video Video to Text (MSR-VTT) [2]

## Model
Developed 2 CNN-RNN architectures for video caption generator.
CNN architectures are used for visual encoding and RNN structures are used for decoding.
1. Fixed Representational Context [3]

![](sample/model1.png?raw=true)

2. Sequence to Sequence [4]

![](sample/model2.png?raw=true)

## Sample result on testing data

| Video | Text (Greedy)|
|-------|----------|
| ![](sample/F2Ny7rq9RKs_139_148.avi.gif?raw=true) | “a person is adding ingredients into a bowl”|
| ![](sample/r2oI9Y-3wAo_21_28.avi.gif?raw=true) | “a panda bears is climbing up a bench” |

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
[1] D. L. Chen and W. B. Dolan. Collecting highly parallel data for 4
paraphrase evaluation. 2011. In Proceedings of ACL, pages 190–200.<br>
[2] Jun Xu, Tao Mei, Ting Yao and Yong Rui. 2016. MSR-VTT: A Large Video Description Dataset for Bridging Video and Language. In CVPR 2016.<br>
[3] S. Venugopalan et al. 2014. Translating videos to natural language using deep recurrent neural networks. arXiv preprint arXiv:1412.4729.<br>
[4] S. Venugopalan et al. 2015. Sequence to Sequence - Video to text. In IEEE ICCV<br>

