# LSM6DSV Best Practices

This guide discusses how to achieve great performance (consistent +45 min resets) using trackers with LSM6DSV IMU. You can skip step 1 and 2, if you are using Panda Trackers (LSM6DSV).  

 ## 1. LSM6DSV hardware

Make sure you are using correct chip. There are many LSM6 IMUs but only the **LSM6DSV** is the top model with the best performance. 

You need well designed trackers that follow LSM6DSV design specifications (many SlimeVR designs do not follow this). Recommended well tested designs: Cheesecake and Panda. 

 ## 2. Correct firmware 

 Make sure you are using correct FW: l0ud/sfusion. This FW is well tested on LSM6DSV and provides GREAT and CONSISTENT results. It has been merged with the main SlimeVR/main already, meaning it's very stable and performs consistent.
 
 There are many versions of sfusion, do not mistake them. Do not use kounocom/sfusion-tuned-mbe or any FW like that. Do not use any of MBE firmwares, those are expirimentaly, have many bugs and do not provide consistent results.

 ## 3. 6 sides calibration

Make sure you have done the LSM6DSV IMU [6 sides calibration](docs/imu-calibration.md) correctly.  

 ## 4. Using LSM6DSV trackers

Always place trackers on a stable surface (table or floor) and turn them on. Wait a few seconds for sensors to initialize. A common mistake is putting trackers on your body and turning them on, which will increase drift a lot.

You need to warm your trackers each time your start them. There are many ways to do it but the simplest one is to turn them on and play for 20 min. Trackers will reach stable working temperature after that. You need to take trackers off and place on the stable surface like floor and leave to sit for a few seconds, so sensor could recalibrate at a working temperature. You can put your trackers back on and continue playing, enjoying +45 min resets now! 

Return Panda Trackers [main README.md](../README.md) 


