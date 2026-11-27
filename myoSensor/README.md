
# sEMG Gesture Detection (Summer 2025)

I created PCBs to sense the electric signals in my forearm. The ESP32 reads the data, filters it, then runs on-device inference to determine the hand gesture.

<img width="375" height="270" alt="emg_live_demo_compressed" src="https://github.com/user-attachments/assets/85866ee6-9dae-4d0d-815e-a1579a4ceb0d" />


```mermaid
flowchart TD
    A["sEMG Electrodes"] --> B["Amplifier PCB"]
    subgraph ESP32
        C["ESP32 ADC"] --> D["Digital Filtering"]
        D --> E["On-Device Inference"]
        subgraph InferenceModel["Keras Model (2-ch Window)"]
            direction TB
            M1["Conv1D(32, k=5, relu6)"] --> M2["GlobalMaxPooling1D()"]
            M2 --> M3["Dense(4, softmax)"]
        end
        E -.-> M1
    end
    B --> C
    M3 --> F["Gesture Prediction"]
```


---


Running the model on an ESP32 microcontroller proved difficult, restricting the types of layers I could use in the neural network in addition to having limited memory. By pivoting to a simpler Conv1D-based model I was able to successfully deploy the model for live inference. 


---


<img style="width: 35%; height: auto;" alt="IMG_3330" src="https://github.com/user-attachments/assets/84e07083-6847-4aa9-a37d-03ca40f99430" />

The sensors are mounted directly to the forearm.







