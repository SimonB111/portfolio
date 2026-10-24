# sEMG Gesture Detection (Summer 2025)

I created PCBs to sense the electric signals in my forearm. The ESP32 reads the data, filters it, then runs on-device inference to determine the hand gesture.

https://github.com/user-attachments/assets/ff40a174-9609-4921-ad33-305a34994136


---


Running the model on-device proved difficult, restricting the types of layers I could use in addition to having constrained memory. By pivoting to a simpler Conv1D-based model I was able to successfully deploy the model for live inference. 


---


<img style="width: 40%; height: auto;" alt="IMG_3330" src="https://github.com/user-attachments/assets/84e07083-6847-4aa9-a37d-03ca40f99430" />

The sensors are mounted directly to the forearm.







