# SWELL-KW
Multimodal SWELL knowledge work (SWELL-KW) dataset for research on stress and user modeling. 

# DATASET
The dataset used in this repository could be found here https://www.kaggle.com/qiriro/swell-heart-rate-variability-hrv

# BACKGROUND
This dataset comprises of heart rate variability (HRV) indices computed from the multimodal SWELL knowledge work (SWELL-KW) dataset for research on stress and user modeling (see. http://cs.ru.nl/~skoldijk/SWELL-KW/Dataset.html). The SWELL was collected by researchers at the Institute for Computing and Information Sciences at Radboud University. It is a result of experiments conducted on 25 subjects doing typical office work (for example writing reports, making presentations, reading e-mail and searching for information). The subject went through typical working stressors such as receiving unexpected emails interruptions and pressure to complete their work on time. The experiment recorded various data including computer logging, facial expression, body postures, ECG signal, and skin conductance. The researchers also recorded the
subjects’ subjective experience on task load, mental effort, emotion, and perceived stress. Each participant went through three different working conditions:

No stress: the subjects are allowed to work on the tasks as long as they needed for a maximum
of 45 minutes but they are not aware of the maximum duration of their tasks.

Time pressure: during this time, the time to finish the task was reduced to 2/3 of the time the participant took in the neutral condition.

Interruption: the participants received eight
emails in the middle of their assigned tasks.
Some emails were relevant to their tasks —and
the participant was requested to take specific
actions—while others were just irrelevant to
their tasks.

# HRV COMPUTATION
HRV indices were computed as follows: First, the researchers extracted an inter-beat interval
(IBI) signal from the peaks of the Electrocardiography (ECG) of each subject. Then, each HRV
index is computed on a 5 minutes IBI array. A new IBI sample is appended to the IBI array while the
oldest IBI sample is removed from its beginning. The new resulting IBI array is used to compute
the next HRV index. This process is repeated until the end of the entire IBI signal. Unlike other
HRV computation methods proposed by other researchers —which mostly consist of computing
HRV on the whole signal, it was noticed that this approach allows a more
granular, detailed and accurate study of how each heartbeat influences the person’s HRV.

# RESEARCH CONTRIBUTION
The original dataset contains raw ECG signal and a feature dataset which is annotated with the conditions under which the data was collected. It also contained heart rate variability (HRV) feature (only RMSSD) that was computed every one minute. For more details, refer to the published paper included in this repository.

# NOTEBOOK
The notebook analyzes the finalized dataset having 36 features. The notebook employs a "Random Forest Classifier" which predicts the stressor label (No stress,Time Pressure,Interruption) using the remaining extracted features. The classification report is then returned.
