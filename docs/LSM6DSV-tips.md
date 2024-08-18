# LSM6DSV Best Practices

This guide discusses how to achieve great performance (consistent +45 min resets) using trackers with LSM6DSV IMU. You can skip hardware and firmware parts, if you are using Panda Trackers (LSM6DSV).  

 ## LSM6DSV hardware

Make sure you are using a correct chip. There are many LSM6 family IMUs (example LSM6DSO, LSM6DSR) but only the **LSM6DSV** is the top model with the best performance. 

You need well designed trackers that follow LSM6DSV design specifications (many SlimeVR designs do not follow this). Recommended well tested designs: Cheesecake and Panda. Get [Panda Trackers](https://discord.gg/ZzgH7QkN7F). 

There are a few reports of faulty LSM6DSV IMU boards from some SlimeVR sellers but not enough data to confirm yet. It's possible to damage your IMU building DIY trackers. It's possible there are just bad DIY tracker designs for LSM6DSV. Main issues on tiny SlimeVR trackers that do not follow LSM6DSV design guidelines and place other componnents too close to the IMU sensor. 

 ## Correct firmware 

 Make sure you are using correct FW: [l0ud/sfusion](https://github.com/l0ud/SlimeVR-Tracker-ESP-BMI270/tree/sfusion). This FW is well tested on LSM6DSV and provides GREAT and CONSISTENT results. It has been merged with the main SlimeVR/main already, meaning it's very stable and performs consistent.
 
 There are many versions of sfusion, do not mistake them. Do not use kounocom/sfusion-tuned-mbe or any similar sfusion FWs. 
 
 Do not use any of MBE firmwares, those are expirimentaly, have many bugs and do not provide consistent results yet.

 ## Six sides calibration

Make sure you have done the LSM6DSV IMU [6 sides calibration](imu-calibration.md) correctly.  

 ## Using LSM6DSV trackers

Always place trackers on a stable surface (table or floor) and turn them on. Wait a few seconds for sensors to initialize. A common mistake is putting trackers on your body and turning them on, which will increase drift a lot.

You need to warm your trackers each time your start them. There are many ways to do it but the simplest one is to turn them on and play for 20 min. Trackers will reach stable working temperature after that. You need to take trackers off and place on the stable surface like floor and leave to sit for a few seconds, so sensor could recalibrate at a working temperature. You can put your trackers back on and continue playing, enjoying +45 min resets now! 

Visit Panda Trackers Discord for more info and help https://discord.gg/ZzgH7QkN7F

Return Panda Trackers [main README.md](../README.md) 


