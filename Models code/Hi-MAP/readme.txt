Source: Fabbri et al. (2019)

==
The original code is from OpenNMT:http://opennmt.net/

We adapted their code and implemented our Hi-MAP model.

==
Main changes:

Preprocessing in onmt/inputters/text_dataset.py: we extend one more field.

MMR scores in onmt/decoders/decoder.py: add _run_mmr_attention() function.

Sentence level encoder in onmt/encoders/rnn_encoder.py

==

Use python 3.6 to run


* Pre-processing

Execute run_preprocessing_himap.sh

* Train

Execute run_train_himap.sh

* Inference

Execute run_inference_himap.sh for the Multi-News summaries

Execute run_inference_himap_homicide.sh for the Homicide summaries

The result will be a large file, each line is a record.
