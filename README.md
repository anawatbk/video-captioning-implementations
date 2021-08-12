# video-captioning-implementations

Goal：

- Use the architecture in the paper as a reference to reproduce our own version

- Understand the model framework, e.g. Encoder-Decoder, seq2seq

- Build various architectures and compare the result

Methods attempted：Two CNN - RNN Architecture

- CNN architectures are used for visual encoding
- RNN structures are used for decoding

Technical details:

- Generated visual encoding vectors from each video using resnet50/VGG16
  - Reduce training time
  - Extract high-level features

- Used google-news word2vec for language encoding

- Implemented encoder and decoder from scratch
  - Figure out the variable size in each neural network layer
  - Create pipelines for the seq2seq model

- Implemented Teacher Forcing for RNN from scratch

Highlight:
- Gradient Clipping saved us from vanishing/exploding gradient problem

Potential improvement:
- Add attention layers                          
- Implement dense video captioning
