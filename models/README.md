# Models and vocabularies
Repository of links to download pre-trained parameters and vocabularies of **pre-trained Bidirectional Language Models**.

In a terminal, type `tar -xvzf filename.tgz` to extract the folder with at least 4 files of the pre-trained Bidirectional Language Model ({lang} is the language symbol like fr for French). When the SentencePiece tokenizer has been used, there are 2 more files (SentencePiece model and vocab from the General language Model). The file tgz was created by the command `tar -cvzf filename.tgz /path/to/source/folder`.
- Forward LM:
  - pre-trained parameters: {lang}_wt.pth
  - vocabulary: {lang}_wt_vocab.pkl
- Backward LM:
  - pre-trained parameters: {lang}_wt_bwd.pth
  - vocabulary: {lang}_wt_vocab_bwd.pkl
- SentencePiece:
  -  model: spm.model
  -  vocab: spm.vocab

For each Language Model, the link to the corresponding notebook is done. It allows to understand how the LM was trained and on which training corpus.

## Portuguese Bidirectional LM

I trained a Portuguese Bidirectional Language Model with the MultiFit configuration (see accuracy and perplexity on the [Language Models page](https://github.com/piegu/language-models)).

### Configuration MultiFiT (architecture 4 QRNN with 1550 hidden parameters by layer / tokenizer SentencePiece (15 000 tokens))
- [pt_lm_sp15_multifit.tgz](https://drive.google.com/uc?id=1NmH1Ug1YeontgAlgbvZxNZ115WNoZNjq) (185 Mo, 6 files) | notebook [lm3-portuguese.ipynb](https://github.com/piegu/language-models/blob/master/lm3-portuguese.ipynb) | Training corpus: 100 millions tokens from Portuguese Wikipedia

## French Bidirectional LM

I trained 3 French Bidirectional Language Models but the best is the one trained with the MultiFit configuration (see accuracy and perplexity on the [Language Models page](https://github.com/piegu/language-models)).

### 1. Configuration MultiFiT (architecture 4 QRNN with 1550 hidden parameters by layer / tokenizer SentencePiece (15 000 tokens))
- [fr_lm_sp15_multifit.tgz](https://drive.google.com/uc?id=1AZuCn4BkuXiFRebo0krk6svx09Bgrxvt) (185 Mo, 6 files) | notebook [lm3-french.ipynb](https://github.com/piegu/language-models/blob/master/lm3-french.ipynb) | Training corpus: 100 millions tokens from French Wikipedia

### 2. Architecture QRNN / tokenizer SentencePiece
- [fr_lm_qrnn_sp15.tgz](https://drive.google.com/uc?id=1cAVj40tI9Q4RVrmn-AzF6dER8xTv1_zM) (200 Mo, 4 files, the 2 SP files are missing) | notebook [lm2-french.ipynb](https://github.com/piegu/language-models/blob/master/lm2-french.ipynb) | Training corpus: 100 millions tokens from French Wikipedia

### 3. Architecture AWD-LSTM / tokenizer spaCy
- [fr_lm_awdlstm_spacy.tgz](https://drive.google.com/uc?id=1CN6QqTxnTy_UHVTaIqc53mwSVpJJZtbN) (315 Mo, 4 files) | notebook [lm-french.ipynb](https://github.com/piegu/language-models/blob/master/lm-french.ipynb) | Training corpus: 100 millions tokens from French Wikipedia


