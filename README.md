# RNN-tv_script_generation

First of all, I'd like to thank Prof. Vijay Kumar from MSRIT(HOD of Info science) and Abhijith Chandraprabhu from Julia Computing for having provided this opportunity to participate in Computational Machine Learning(CML) course organised at IISc under their tutelage as a part of CCE(Center for Continuing Education). Julia is truly an incredible language. The ease and speed of programming in Julia is impressive!



 This project was carried out in Alenware2015 edition with following hardware configurations. Processor: 2.5GHz, Intel Core i7 Meomry: 16GB 1600 MHz DDR3 Graphics: nvidia GTX970 4gb
 
 
 In this project, I built a recurrent neural network (RNN) capable of creating ridiculous Simpson's tv scripts.

Summary
Dataset
The dataset for this project was a selection of scenes in Moe's Tavern in The Simpson's. See here.

Project Steps
All the work done in this project is in the dlnd_tv_script_generation jupyter notebook.

Pre-process the data by:
Making look-up dictionaries where a word is represented by an integer and vice versa, as the vocabulary list is converted to integers.
Tokenizing the punctuation within the scripts to make sure the network knows "bye" and "bye!" are the same, regardless of surrounding punctuation.
Build the inner workings of the RNN, including determining how many LSTM layers to use (I initally wanted two but found one trained much easier) and utilizing dropout with a wrapper function.
Create an embedding layer for use with the inputs before the LSTM layer(s).
Build the full RNN, using the embedding, LSTM layer(s), and a fully connected layer for determining the following word based on an input.
Making a function to grab batches of training data.
Tuning hyperparameters.
Training the neural network.
Testing it out on a feed word to see whether it can generate a somewhat comprehensible script.
