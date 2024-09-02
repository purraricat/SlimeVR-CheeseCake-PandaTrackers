# LSM6DSV Best Practices

This guide discusses how to achieve great performance (consistent +45 min resets) using trackers with LSM6DSV IMU. You can skip hardware and firmware parts, if you are using Panda Trackers (LSM6DSV).  

 ## Six sides calibration

Make sure you have done the LSM6DSV IMU [6 sides calibration](imu-calibration.md) correctly.  

 ## Using LSM6DSV trackers

To start your VR session, always place trackers on a stable surface (table or floor) and turn them on. Wait a few seconds for sensors to initialize. A common mistake is putting trackers on your body and turning them on, which will increase drift a lot.

You need to warm your trackers each time your start them. There are many ways to do it but the simplest one is to turn them on and play for 20 min. Trackers will reach stable working temperature after that. You need to take trackers off and place on the stable surface like floor and leave to sit for a few seconds, so sensor could recalibrate at a working temperature. You can put your trackers back on and continue playing, enjoying +45 min resets for the rest of the session! 

Visit Panda Trackers Discord for more info and help https://discord.gg/ZzgH7QkN7F

Return Panda Trackers [main README.md](../README.md) 

 ## Extra info for DIY LSM6DSV (non Panda trackers) 

 ## LSM6DSV hardware

Make sure you are using a correct chip. There are many LSM6 family IMUs (example LSM6DSO, LSM6DSR) but only the **LSM6DSV** is the top model with the best performance. 

You need well designed trackers that follow LSM6DSV design specifications (many SlimeVR designs do not follow this). Recommended well tested designs: Cheesecake and Panda. Get [Panda Trackers](https://discord.gg/ZzgH7QkN7F). 

There are a few reports of bad performance of LSM6DSV trackers from some SlimeVR market sellers but not enough data to comfirm if it's hardware design flaws or just wrong firmware and settings. It's possible to damage your IMU building DIY trackers too. 

 ## Correct firmware 

 Make sure you are using correct FW: [l0ud/sfusion](https://github.com/l0ud/SlimeVR-Tracker-ESP-BMI270/tree/sfusion) (a backup Panda Trackers [LSM sfusion](https://github.com/purraricat/Panda-Trackers-LSM-sfusion/tree/sfusion)). This FW is well tested on LSM6DSV and provides GREAT and CONSISTENT results, it has been merged to the main SlimeVR/main now. Do not use the SlimeVR/main though, it will still provide worse reset times over original sfusion. Make sure you are flashing the correct l0ud/sfusion brach and not just the default l0ud/main too. You can use [web flasher](https://slimevr-firmware.unlogisch.ch) for easy flashing. 
 
 There are many versions of sfusion, do not mistake them. Some may sound better and have extra features added like sfusion-tcal or dynamic-sfusion but all have delivered worse reset times over the original l0ud/sfusion then tested. 
 
 Do not use any of MBE firmwares, those are expirimental and have many bugs. MBE requires extra calibration steps before every session too. MBE fw are not optimized and will cause issues on the esp-12f used in Pandas and Cheesecakes. 
