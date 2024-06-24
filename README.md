# NLP-Sequence-classification
Sequence classification for abbreviation and long form detection

PLOD-CW dataset consists of training, validation and testing sets structured for the purpose of sequence classification, specifically for detecting abbreviations and long-forms. As multiple tokens/words can belong to the same long-form, BIO format[1] labelling schema is adapted.
Training, Testing and Validation data from PLOD dataset comprises of 1072, 126 and 153 rows respectively with tokens, part-of-speech tags and named entity recognition tags.

<img width="818" alt="Screenshot 2024-06-24 at 11 58 36" src="https://github.com/sneha-h/NLP-Sequence-classification/assets/7019246/e1065196-903a-4bdc-98fd-15d0e8baeb07">


Understanding of BIO schema with an example:
[For, this, purpose, the, Gothenburg, Young, Persons, Empowerment, Scale, (, GYPES, ), was, developed, .]
[B-O, B-O, B-O, B-O, B-LF, I-LF, I-LF, I-LF, I-LF, B-O, B-AC, B-O, B-O, B-O, B-O]
GYPES - B-AC - Abbreviation
Gothenburg - B-LF - Beginning Long Form Young - I-LF - Inside Long Form
Persons – Inside Long Form

Condicted various experiments using different vectorization techniques (TF-IDF, Bag Of Words, Hashing, Spacy, Glove) and with algorithms including (SVM, FFNN, RNN, LSTM and Transformer-based model like DistilBert), the Transformer model DistilBert performed the best.

Results from transformer based model DistilBert:

<img width="847" alt="Screenshot 2024-06-24 at 12 01 49" src="https://github.com/sneha-h/NLP-Sequence-classification/assets/7019246/e455cf6c-b456-414e-928e-b003e0a49f9e">

<img width="979" alt="Screenshot 2024-06-24 at 12 01 23" src="https://github.com/sneha-h/NLP-Sequence-classification/assets/7019246/77882d8c-d4f8-433c-8a4f-d70afce0100f">
