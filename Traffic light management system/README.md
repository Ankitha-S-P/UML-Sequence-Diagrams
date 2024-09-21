# Traffic Light Management System - Sequence Diagram

## Overview

This repository contains a sequence diagram for a **Traffic Light Management System**. It outlines how different components, such as the **Traffic Sensor**, **Central Control System**, and **Traffic Lights**, interact to manage traffic signals in real-time based on sensor data. The diagram also includes a failure handling scenario where a sensor fails to provide data, and the system switches to a default operation mode.

## Sequence Diagram

The sequence diagram demonstrates the following flow:

1. **Data Collection:**
   - The traffic sensor collects traffic data every 5 seconds and sends it to the central control system for analysis.
   
2. **Decision Making:**
   - Based on the traffic conditions (such as the status of the other lane's traffic light and its timer), the central control system decides whether to show a green, yellow, or red light.

3. **Feedback:**
   - After each decision, the central control system receives feedback from the traffic light to confirm the operation.

4. **Error Handling (Sensor Failure):**
   - In case a sensor stops sending data, the system detects the failure and switches to a default traffic light timing mode to ensure continued traffic flow.

## Components Involved

- **Traffic Sensor:** Collects real-time traffic data and sends it to the central control system.
- **Central Control System:** Analyzes sensor data and determines the appropriate traffic light signal based on predefined conditions.
- **Traffic Lights:** Adjust based on the instructions from the central control system and provide feedback on their status.
  
## Notations Used

- **Loop Block:** Repeats the data collection every 5 seconds.
- **Alt Block:** Handles alternate conditions:
  - Green light if the other lane's light is red and its timer is expired.
  - Yellow light if the other lane is red with a timer less than 10 seconds.
  - Red light in all other cases.
  - Sensor failure is also managed through an alternative path.
  
## Error Handling

- The system detects a sensor failure if no data is received, indicated in the `alt` block labeled "sensor failure."
- Upon detecting failure, the system continues with default traffic signal timings to avoid disruption.

## Scalability

The system is scalable to handle additional intersections or traffic lights. The centralized control system would manage data from multiple traffic sensors and adjust traffic lights accordingly.

