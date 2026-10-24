# Neuromorphic Slip-Detecting Robot Gripper (Ongoing)

Detects when object in hand is slipping by amplifying the vibration audio, then compressing and sending to a computer where a spiking neural network (SNN)
classifies the audio. 

<img style="width: 60%; height: auto;" alt="IMG_4355" src="https://github.com/user-attachments/assets/d5c391c0-afa8-4043-a43e-f3ae78c8e106" />


---


My first iteration of the SNN had accuracy issues. By automating data labeling using an IMU for ground-truth slip data,
I was able to significantly improve the performance of the model. Due to the imbalanced nature of the binary classification task (with slip being the minority class),
I focused on improving the F1 since it provides a balance between raw precision and recall.


---


<img style="width: 40%; height: auto;" alt="IMG_4305" src="https://github.com/user-attachments/assets/3b18e725-21d5-4657-ae88-6d9ad1687ee0" />

The amplifier PCB is hand-soldered and includes two amplification stages in addition to filters.
