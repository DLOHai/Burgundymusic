# Burgundy project: Completing 'unfinished' Maestro's musical work
sponsored by Deep Learning College @Modulabs, Seoul, South Korea
contributor: Jinwoo Oh, Wonyoung Seo, Sumin Han

## Model

- Music Transformer: Generating Music with Long-Term Structure
- 2019 ICLR, Cheng-Zhi Anna Huang, Google Brain
- [paper link](https://arxiv.org/abs/1809.04281) 
- [paper review](https://github.com/SSUHan/PaparReviews/issues/13)
- Re-producer : [Yang-Kichang](https://github.com/jason9693/MusicTransformer-tensorflow2.0/)
- Customizer: Jinwoo OH


## Data

To extend Chopin’s unfinished `piano sonata, Canon in F minor, B. 129a`, we trained the model with Chopin's other works in MAESTRO dataset.


## Train

* Train with only Decoder wise ( only self-attention AR. )

  ```bash
  $ python train.py --pickle_dir= './chopin_preroc/' --save_path= './result/'
  ```


## Hyper Parameter

* learning rate : 0.0001
* head size : 4
* number of layers : 6
* seqence length : 2048
* embedding dim : 256 (dh = 256 / 4 = 64)
* batch size : 1
  Because Our memory didn't statisfy the requirement of model (Batch_size = 2), we define it 1.
