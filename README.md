# pytorch-sentiment-neuron
Requires pytorch, cuda and python 3.5

Sample command :

python visualize.py -seq_length 1000 -cuda -load_model mlstm_ns.pt -temperature 0.4 -neuron 2388 -init "I couldn't figure out"

The lm.py file allows you to train the model on new data. For instance :

python lm.py -seq_length 50 -batch_size 64 -rnn_size 4096 -embed_size 64 -layers 1 -learning_rate 0.001 -cuda -load_model mlstm_ns.pt -save_model mlstm -rnn_type mlstm -dropout 0 -train data/your_input_file.txt -valid data/your_validation_file.txt
