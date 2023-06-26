# EEG Motor Imagery Classification Using CNN, Transformer, and MLP


 <p align="center"> <img src="https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/assets/cnn-transformer-mlp-white.png" alt="CNN-Transformer-MLP" > An illustration of the CNN-Transformer-MLP model. </p>


The electroencephalogram, or EEG for short, is one of the biosignals that display brain activity in the form of time-series data. EEG can be used to help amputees or paralyzed people move their prosthetic arms via a brain-computer interface (BCI). In order to identify the correct limbs to control from the EEG signal, a combination of CNN, Transformer, and MLP is utilized in this work for motor imagery (MI) classification. CNN converts the epoched EEG signal into meaningful representation in accordance with the signal's non-stationary nature. Transformer finds the global relationship of the given representation from CNN. MLP classifies the expected upper limbs to move based on the extracted information from the Transformer. To gauge the capability of the CNN-Transformer-MLP model, PhysioNet's EEG Motor Movement/Imagery Dataset is used. The model attains an accuracy of ``76.4%`` in the test set.


## Experiment

To run the experiment, [click here](https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/EEG_Motor_Imagery_Classification_Using_CNN_Transformer_and_MLP.ipynb).


## Result

### Quantitative Result
To quantitatively validate the capability of the CNN-Transformer-MLP model, certain evaluation metrics are employed: accuracy and loss. Accuracy measures how many times the model makes a correct prediction in a particular split of the dataset. Loss quantifies how close the prediction is to the actual label. The loss calculation is utilized in the training stage as well. In this work, the binary cross-entropy (BCE) loss is adopted for the loss function.

Dataset Split | Accuracy | Loss
------------ | ------------- | -------------
Train | 82.9% | **0.201** 
Validation | **84.4%** | 0.269
Test | 76.4% | 0.856


### Accuracy and Loss Curve

 <p align="center"> <img src="https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/assets/accuracy_curve.png" alt="acc_curve" > <br /> Accuracy curve on the train set and the validation set. </p>
 
  <p align="center"> <img src="https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> Loss curve on the train set and the validation set. </p>

### Qualitative Result

Here, the qualitative performance of the model is presented.

<p align="center"> <img src="https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/assets/true_right.png" alt="true_right" > <br /> Correct prediction on the right arm class. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/assets/true_left.png" alt="true_left" > <br /> Correct prediction on the left arm class. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/eeg-motor-imagery-classification/blob/master/assets/false_right.png" alt="false_right" > <br /> False prediction on the left arm class. </p>

## Credit

- [Timeseries Classification With a Transformer Model](https://keras.io/examples/timeseries/timeseries_classification_transformer/)
- [EEG Classification](https://github.com/DavidSilveraGabriel/EEG-classification/blob/master/Using_mne_and_braindecode.ipynb)
- [Loading EEG Data](https://neuro.inf.unibe.ch/AlgorithmsNeuroscience/Tutorial_files/DataLoading.html)
- [MNE-Python](https://mne.tools/stable/glossary.html)
- [Self-Attention and Positional Encoding](https://d2l.ai/chapter_attention-mechanisms-and-transformers/self-attention-and-positional-encoding.html)
