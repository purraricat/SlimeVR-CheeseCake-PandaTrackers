## IMU Sensor calibration

This guide is specifically for the LSM6DSV IMU calibration but you can use same steps for BMI160, BMI270 and LSM6DSO models too. 

6 sides calibration needs to be done only once after you get or build your new tracker set.

  - For best results, **calibrate when the trackers are warmed up** - turn them on and wear them for 20 minutes,
    wait for the temperature to stabilize at 30-40 degrees C, only then calibrate.

    Enable developer mode in SlimeVR settings to see tracker temperature.

### LSM6DSV - 6 sides calibration

  - **Step 0: Turn off the tracker. Flip it upsidedown and turn power on.**
    
    > The LED will be lit continuously. Wait for 2s and flip tracker back up while the LED is still solid. Wait, do not move the tracker.
    
  - **Step 1: Make sure tracker does not move, the LED will flash 3 times when gyroscope calibration begins.**
    
  - **Step 2: LED will flash 6 times when accelerometer calibration begins and it will flash 2 short blinks that the current side has been recorded.**

    > The accelerometer calibration process requires you to **hold the device in 6 unique orientations** (e.g. sides of a cube),
    > keep it still, and not hold or touch for 3 seconds each. It uses gravity as a reference and automatically detects when it is stabilized - this process is not time-sensitive.

    > If you are unable to keep it on a flat surface without touching, press the device against a wall, it does not have to be absolutely perfect.

    **There will be two very short blinks when each position is recorded.**
    
    Rotate the device 90 or 180 degrees in any direction. It should be on a different side each time. Continue to rotate until all 6 sides have been recorded. I like rotating tracker on one axis 90' degrees to record all 4 sides, then flip axis to record 2 sides left. This makes keeping track of recorded sides easy.

    Watch calibration video - https://www.youtube.com/watch?v=0kHLL7mCRfo
    
    The last position has a long flash when recorded, then LED will start blinking normaly and tracker will appear connected in the SlimeVR server. All calibration data has been saved on the tracker and you can turn it off safely now. 

If tracker has an extension, you need to repeat the same steps turning the tracker off, flipping the extension upsidedown and turning the tracker on, and follow the LED just like you did before to record all 6 sides of the extension.   

  #### Additional info  

   If you have any problems with this procedure, connect the device via USB and open the serial console to check for any warnings or errors that may indicate hardware problems.
  
If you have the tracker connected via USB and open the serial console, you will see text directions in addition to the LEDs. This can help to calibrate the tracker and understand the procedure. Use this only for learning the process.

Calibration will be bad with USB cable plugged because it will pull on the board and generate heat charging the tracker too. So to get a good calibration always redo it without the USB cable plugged and just follow the LED light.


Return Panda Trackers [main README.md](../README.md) 

