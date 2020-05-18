# Vietnamese-Word-Vectors
Word vectors for Vietnamese using Fasttext

[Fasttext model](https://drive.google.com/open?id=1ktHmHxoqV1iab3vWDeRmiGDg9v9hGshF)

Tokenized using VncoreNLP

In English, the majority of words are 1 complete token
In Vietnamese, it's the opposite, 1 token can be a word, or 2, or even 3
e.g: 
dòng nước lũ = floodwater
'dòng' + 'nước' + 'lũ' each is one token, total òf 3 tokens
flood


One problem in embedding Vietnamese is most of the words standalone have multiple meaning, and usually make more specific sense in phrases
-> hard to evaluate model

plural and singular in Vietnamese aren't just usually noun with 's'
-> analogy task won't work well

Analogy task in Vietnamese:
analogies list translate from english doesn't work well since in Vnmese, most of them are pharses, not words or tokenized phrase to word
both fasttext default model and vnnews model work mediocrely

fasttext default wiki model work better with city analogy test - more data 

Neareast neighbour:
Work decently in both models

Similarity task:
Using ViSim dataset for the task
Words pair with opposite meaning/ similar meaning on a scale judge by human
In progress

Both models have some uncleaned data that affect the evaluation task, e.g bố ~ bốbố 0.6745...
