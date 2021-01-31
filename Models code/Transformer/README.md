Source: Fabbri et al. (2019)

### Preprocess
To get the training and validation data in OpenNMT format, you first need to preprocess the input data. The raw data should be in text files with one record per line. You need to modify the path to text files in the `run_preprocess.sh` before running the script.
```sh
$ ./run_preprocess.sh
```

### Training
We used the same training parameters as on OpenNMT Summarization page. 
```sh
$ ./run_train_transformer.sh
$ ./run_train_transformer_colab.sh
```

### Testing
To test the model on test data:
```sh
$ ./run_test_transformer.sh
$ ./run_test_transformer_colab.sh
$ ./run_test_transformer_homicide.sh
```
