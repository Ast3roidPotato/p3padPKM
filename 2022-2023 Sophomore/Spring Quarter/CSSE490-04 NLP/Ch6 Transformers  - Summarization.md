## Intro

Summarization is a difficult task that requires an understanding of the document, understanding the context of the document, and having domain specific knowledge. 

Summarization is a sequence to sequence problem (seq2seq) which is tackled well by encoder-decoder transformers.

## The CNN/DailyMail Dataset

Summaries consist of new sentences instead of just simple extracted sentences.

Explores Several Models:
- GPT-2
- T5
- BART
- PEGASUS

GPT-2 tends to hallucinate and invent facts.

## Measuring the Quality of Generated Text

It's hard to evaluate generated text because there are multiple valid outputs.

Two common evaluation metrics are:
- BLEU
- ROUGE

BLEU is a precision based metric that counts n-grams in the generated text and compares it to the reference text. 

