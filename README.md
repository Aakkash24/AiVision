# AiVision
AiVision is an AI based software designed to automate the process of manually monitoring the surveillance system, detects threats and alerts the concerned authorities.

Project flow:
1. Violence detection:
The CCTV frames will be fed into the model lively and the model will try to predict if the frame contains violence. A threshold of upto 30 frames is set to confirm that a violence is occuring in the place. So, the violent frame is saved and the next step is to figure out any suspects in the frame. This prediction part is done on the top of MobileNetV2 model

2. Face detection:
Given that a violence is happening in the place, the model calls another function to detect suspects involved in the last violent identified frame and stores them. The face detection part is done using the PIL

3. Alerting the concerned authorities:
Now the violent frame and the image with suspects is saved. To alert the authorities, we have integrated an Telegram Bot with which the detials of the incident will be alerted on the go.
