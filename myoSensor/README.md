# sEMG Gesture Detection

The goal of this project is to detect which of 4 hand gestures the user is making by analyzing surface electromyography (sEMG) sensor data.
A key constraint is that the ESP32 microcontroller itself was both reading the sensor data and running embedded ML to interpret the data.
I created PCBs to amplify the myoelectric signals and trained a Conv1D-based model with TensorFlow and Keras.

## Hardware & Physical Outputs
![Final Assembled Prototype](./images/prototype.jpg)
*Figure 1: Fully assembled prototype after stress testing.*

## Key Specifications
* **Materials:** 3D printed PETG, CNC routed 3mm carbon fiber
* **Dimensions / Weight:** 220mm wheel base, 340g frame weight
* **Software / EDA Used:** SolidWorks, KiCAD

## Design & Iteration
![CAD Model Render](./images/cad_render.png)
*Figure 2: CAD exploded view showing component placement.*

- **Challenge:** Reducing frame vibration while maintaining structural rigidity.
- **Solution:** Integrated TPU vibration damping mounts for the flight controller.
