ECG Classification using CNNs

This project was conducted in the Signal and Image Processing Lab of the Electrical Engineering Faculty at the Technion, under the supervision of Dr. Meir Bar Zohar. The goal of the project was to classify human ECG signals into three categories: NSR (normal sinus rhythm), ARR (atrial premature beat), and CHF (congestive heart failure). To do this, we used a convolutional neural network (CNN) to classify ECG signals.

Data

The Physionet database is a publicly available collection of ECG signals recorded from various sources, including ambulatory and inpatient settings. It contains 162 recordings of 512-second ECG signals, with a sampling frequency of 128 Hz. The database includes a diverse range of signals, including normal and abnormal rhythms, as well as signals from healthy individuals and those with various cardiac conditions.

For this project, we preprocessed the ECG signals by cutting them into shorter segments and applying the Continuous Wavelet Transform (CWT).



Methods

The CWT is a mathematical tool that decomposes a signal into a series of wavelets, each with a different frequency and scale. This allows for the analysis of both local and global features in the signal. The CWT is particularly well-suited for analyzing ECG signals because it can capture both the high-frequency details (e.g., individual heartbeats) and the low-frequency trends (e.g., long-term changes in heart rate) present in the signal. The CWT coefficients that result from this transformation can then be transformed into images using OpenCV.

To classify the ECG signals, we used transfer learning with a pre-trained GoogLeNet model in PyTorch. We fine-tuned the model on the transformed images, using labels indicating the corresponding heart situation (NSR, ARR, or CHF).

We evaluated the performance of the classifier using various metrics, including accuracy, precision, and recall.



Results

Our classifier achieved an accuracy of XXX%, a precision of XXX%, and a recall of XXX%.


Conclusion

This project demonstrates the effectiveness of using CNNs for ECG classification. The use of transfer learning with a pre-trained model allowed us to achieve good performance with a relatively small dataset. Further work could include exploring other machine learning approaches or expanding the dataset to include a wider range of heart situations.

Usage

To use this project, you will need to install the following dependencies:
