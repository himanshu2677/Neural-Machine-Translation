# Neural-Machine-Translation
English to Hindi Translation

Dataset: https://www.cfilt.iitb.ac.in/iitb_parallel/

Preprocessing:
1. lower the text
2. removing extra spaces
3. replacing numbers with 'num'
4. removing english characters in hindi sentence
5. Filtered to keep only examples with length of English text as well as Hindi text less than 32


Textvectorizer and Text embeddings:
1. Using Fasttext pretrained english and hindi words common-crawl embeddings
2. english text vectorizer is created by setting its dictionary to fasttext english words (Vocabulary size = 2e5)
3. hindi text vectorizer is created by setting its dictionary to fasttext hindi words (Vocabulary size = 2e5)


Models:

1. LSTM: Single layered LSTM model.

    Vocabulary size = 2e5
    Hidden Units = 1024

2. LSTM with Attention: Single layered LSTM model with Attention mechanism. Before each prediction, Decoder can ATTEND to the encoded states at each timestamp from Encoder.

    Vocabulary size = 2e5
    Hidden Units = 1024

  LSTM with Attention is faster to train (reaches low loss finction early) and gets better results than just LSTM.


Evaluation:

1. Bleu-1 scores:
                 LSTM: 0.26479325
  LSTM with Attention: 0.29873173

2. Bleu-2 scores:
                 LSTM: 0.10060721
  LSTM with Attention: 0.12846793

  

