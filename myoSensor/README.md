# sEMG Gesture Detection

The goal of this project is to detect which of 4 hand gestures the user is making by analyzing surface electromyography (sEMG) sensor data.
A key constraint is that the ESP32 microcontroller itself was both reading the sensor data and running embedded ML to interpret the data.
I created PCBs to amplify the myoelectric signals and trained a Conv1D-based model with TensorFlow and Keras.


