# sEMG Gesture Detection (Summer 2025)

I created PCBs to sense the electric signals in my forearm. The ESP32 reads the data, filters it, then runs on-device inference to determine the hand gesture.

https://github.com/user-attachments/assets/ff40a174-9609-4921-ad33-305a34994136


---

<img width="681" height="525" alt="semg_conf_matrix" src="https://github.com/user-attachments/assets/20fb1ae3-5938-49f8-83ce-d3ec46e732b3" />
The 

Running the model on-device proved difficult, restricting the types of layers I could use in the neural network in addition to having limited memory. By pivoting to a simpler Conv1D-based model I was able to successfully deploy the model for live inference. 


---


<img style="width: 35%; height: auto;" alt="IMG_3330" src="https://github.com/user-attachments/assets/84e07083-6847-4aa9-a37d-03ca40f99430" />

The sensors are mounted directly to the forearm.







