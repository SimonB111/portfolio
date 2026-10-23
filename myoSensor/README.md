# sEMG Gesture Detection

<video src="https://github.com/user-attachments/assets/ff40a174-9609-4921-ad33-305a34994136" width="400" controls></video>

The goal of this project is to detect which of 4 hand gestures the user is making by analyzing surface electromyography (sEMG) sensor data.
A key constraint is that the ESP32 microcontroller itself was both reading the sensor data and running embedded ML to interpret the data.
I created PCBs to amplify the myoelectric signals and trained a Conv1D-based model with TensorFlow and Keras.



