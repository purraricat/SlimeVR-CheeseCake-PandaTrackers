# SlimeVR IMU Comparison
A comparison of currently popular IMUs for SlimeVR trackers.  

## Index
- [LSM6DSV](#lsm6dsv)
- [LSM6DSO](#lsm6dso)
- [BMI270](#bmi270)
- [BMI160](#bmi160)
- [BNO085](#bno085)
- [MPU9250](#mpu9250)
- [MPU6500](#mpu6500)
- [MPU6050](#mpu6050)
- [Addendum](#addendum)

## Criteria
We rank these chips in the following categories: Reset Time, Cost, Availability and Build quality.
These factors are meant to give a quick indication as to what to expect from various IMUs, your mileage may vary.
For clarification purposes: If 3 out of 10 chips are dead on arrival or die during early use, we refer to that as poor build quality.

## General Recommendations
At the moment, LSM6DSV is the best IMU in terms of performance offering consistent +45min resets. The BMI160 / BMI270 are the best price-to-performance options. Neither LSM or BMI requires a stable magnetic environment, making them a suitable option for everyone. BNO085 IMU is heavily promoted by the Slime CrowdSupply project but it's an outdated model, with performance comparable to the budget BMI models, yet at a huge price premium, making BNO085 the worst price-to-performance option. 

When referring to the order of the IMUs on this page, bear in mind that they're listed roughly in order of best to worst.

---
## LSM6DSV
The LSM6DSV is a newest IMU for DIY SlimeVR in 2024.  
IMU offers very good reset times, works in bad magnetic enviroments, the best option for VR dancing and fitness use.    

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|40-60 min     |~$12 |Low|Excellent    |



Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i>

|Pros          |Cons                                   |
|--------------|---------------------------------------|
|Accurate               |Low availability              |
|Reliable               |Requires warmup before use    |
|Consistent Reset times |                              |
|Perfect for dancing|                              |

LSM6DSV IMU chips and SlimeVR trackers using this IMU can be bought at [Panda Trackers](https://discord.gg/VPjtkujaVs).

This IMU has been tested for over 3 months, very good performance has been confirmed by over 50 users already. LSM6DSV sfusion firmware is stable and has been merged to the main SlimeVR branch now.

---
## LSM6DSO
Not enough data about this IMU model. 
It's a budget IMU option with a possible performance above the BMI270 but below LSM6DSV. Not enough data to confirm this.

---
## BMI270
The BMI270 is a relatively new and <b>experimental</b> IMU for DIY SlimeVR.
It seems to perform significantly better than the BMI160 while still being affordable.

|Reset time |Cost  |Availability|Build quality|
|:---------:|:----:|:----------:|:-----------:|
|20 - 30min |~$3.8 |Sufficient  |Great        |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-o" ></i>

|Pros                   |Cons                                                            |
|-----------------------|----------------------------------------------------------------|
|Cheap                  | [Requires manual calibration the first time](#imu-calibration) |
|Reliable               | Only available in module form from a single source             |
|Smooth                 | Experimental, still in testing                                 |
|Single time calibration| Performance data not taken from survey                         |

> Please note, that the main branch of SlimeVR firmware does not support this IMU yet, and running a custom fork is required.

---
## BMI160
The BMI160 is the current go-to IMU for DIY SlimeVR.
It is an easily available chip with decent performance and good reliability.

It does not have a magnetometer, but external chips such as QMC5883L/HMC5883L can be used,
in the same way [as with MPU](#mpuqmc5883l). Like any other setup with magnetometers, this is highly experimental.
Reset times and yaw accuracy with a magnetometer will depend on your build quality and magnetic environment.

|Reset time |Cost  |Availability|Build quality|
|:---------:|:----:|:----------:|:-----------:|
|10 - 20min |~$1.50|Sufficient  |Good         |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i><i class="fa fa-star-o" ></i>

|Pros                   |Cons                                                            |
|-----------------------|----------------------------------------------------------------|
|Cheap                  | [Requires manual calibration the first time](#imu-calibration) |
|Reliable               |                                                                |
|Smooth                 |                                                                |
|Single time calibration|                                                                |

---
## BNO085
This is the IMU used in CrowdSupply Slimes. The performance is very unrealiable with very wide range from worst to best reset times. CrowdSupply trackers are sold with a magnetometer turned off because 99% of users will not be able to use that feature having bad magnetic enviroment at home. This will cut the best case reset times down to 20 min, bringing performance down to budget IMU models like BMI. Unlike budget BMI IMUs, BNO085 suffers from additional problems. IMU drift is very high, tracking may even fail moving too fast. For example, BNO085 can drift in just 2 minutes, even stop tracking, if you will start jumping or tap feet while dancing. As a result, this IMU should be avoided for fitness and dance use.   

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|3 - 20 min|~$13 |Sufficient  |Excellent    |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i>

|Pros          |Cons                                   |
|--------------|---------------------------------------|
|Reliable      |Expensive                              |
|Magnetometer        |Magnetometer unsable by 99% users |
|        |High drift rate, even failure to track from fast movements                                       |
|        |Bad price to performance ratio                                       |
|        |Requires warmup before use                                       |


> Please note, there is a lot of misinformation being spread by the SlimeVR CrowdSupply project having an interest selling the exact BNO085 IMU model and trackers.

---
## MPU9250

<b>Not recommended for new designs.</b>

The MPU9250 (currently ran in several modes) is a newer installment of the MPU lineup.

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|10 - 40 min|~$7  |Insufficient|Mediocre     |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o" ></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                                           |
|-----------------|---------------------------------------------------------------|
|Affordable       |Very prone to counterfeit/DOA units                            |
|Smooth           |Sensitive to bad magnetic environments                         |
|Reliable         |[Requires manual calibration the first time](#imu-calibration) |

`Comment: Finding legitimate MPU9250s has become exceedingly difficult due to counterfeits and DOA IMUs. Buy at your own risk.`


---
## MPU6500

<b>Not recommended for new designs.</b>

The MPU6500 is the middle ground of the MPU chips available.
The drift time of this IMU may be a slight improvement over the MPU6050.

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|5 - 10 min |~$1  |Sufficient  |Mediocre     |

Score: <i class="fa fa-star"></i><i class="fa fa-star-half-o"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o" ></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                         |
|-----------------|---------------------------------------------|
|Affordable       |High drift rate                              |
|Available        |More expensive than the 6050 counterpart     |
|Smooth           |Failure rate inconsistent                    |
|                 |[Calibration on each start](#imu-calibration)|

`Comment: Tracking slightly better than the MPU6050.`

---
## MPU6050

<b>Not recommended for new designs.</b>

The MPU6050 will get you started with SlimeVR for cheap.

|Reset time |Cost  |Availability|Build quality|
|:---------:|:----:|:----------:|:-----------:|
|1 - 5 min  |~$1.04|Sufficient  |Poor         |

Score: <i class="fa fa-star"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                         |
|-----------------|---------------------------------------------|
|Cheap            |High drift rate                              |
|High availability|High failure rate                            |
|                 |[Calibration on each start](#imu-calibration)|

`Comment: Order more than you need because of the higher failure rate, it is not uncommon to find 2 to 3 bad chips in a batch.`

---
# Addendum

## What's the difference between an IMU with a magnetometer (9 DOF) and an IMU without a magnetometer (6 DOF)?

IMUs with a magnetometer work like a compass and use the Earth's magnetic field as a reference point to eliminate gyroscope drift, however they require a stable magnetic environment or else they will perform erratically. IMUs without a magnetometer don't require a stable magnetic environment, but are prone to gyroscope drift over time due to being unable to differentiate sensor noise from actual movement, and so will slowly spin in the yaw axis over time. For SlimeVR's purposes, neither is implicitly better or worse than the other. The BNO085, which is the IMU official SlimeVR trackers will use, is used in 6DOF mode and yet performs the best out of all supported IMUs, for example.

## How can I check if I have an acceptable magnetic environment?

You can check by downloading any magnetometer app that shows what your magnetic field strength is in uT and by walking around your playspace. You may want to check at varying heights, such as at chest level, waist level, and ankle level. An option available on both iOS and Android is the app, Physics Toolbox Magnetometer. If you do use Physics Toolbox Magnetometer, you only need to pay attention to the **total**, not the X, Y, or Z components. Most phones have a magnetometer, but if yours does not, then there is no way to be exactly sure of your magnetic environment, but you can make some educated assumptions.

## My app shows around X uT, is that okay?

There's no one value that's acceptable. What matters is that the range of values is low. There is currently limited data to give an exact range, but a good baseline seems to be a range of less than or equal to 5 uT. For example, 20-25 uT would be okay as would 40-45 uT, but a range from 20-40 uT would likely be too unstable to use.

## What determines a "poor magnetic environment"?

Often things made of steel or other ferromagnetic materials contribute most to a poor magnetic environment. Some common examples of things that might affect your magnetic environment include, but are not limited to: spring mattresses, radiators, PC cases, desktop speakers, or furniture that's made of steel. In most cases, the effect that these things will have extend about 6-12 inches (15-30 cm) and within that range may cause the IMU to rotate incorrectly. The size and amount of mass directly impacts the size of the effected area; a paper clip might only affect your IMU if it's directly next to it, whereas a steel bedframe might affect an area 6-12 inches (15-30 cm) away as previous mentioned. In most cases, depending on the size of your playspace, these issues of certain objects causing interference can be mitigated by avoiding or reposition them. Regardless, other factors such as the wiring or rebar in your building could also affect your magnetic environment. These last few examples are harder to predict and illustrate why it's important to test with an app before assuming you might have a stable magnetic environment.

It's also worth mentioning that some controllers have magnets in them, either to hold the battery door closed or for the trigger. As such, placing your controller near a tracker with a magnetometer may cause it to spin slightly.

## Does magnetic interference cause drift?

No, but you may still need to reset. When in an area of magnetic interference an IMU with a magnetometer will reorient itself the same way a compass will when put near a magnet; if you take the magnet away from the compass, the compass will return pointing towards magnetic North. As mentioned though, you may still find yourself needing to reset. For instance, if your bed has a steel bedframe you'll likely need to perform a reset so that your trackers are facing the correct orientation. If you then move somewhere else within your playspace you'll likely then need to reset once again.

## Can I still use my IMU with a magnetometer if I don't have a stable magnetic environment?

This cannot be recommended. When run without the magnetometer, IMUs with magnetometers such as the MPU9250 and ICM20948, perform much worse. That said, if for whatever reason you do want to use your IMU without the magnetometer, the MPU6500 or MPU6050 firmware can be used on the MPU9250 instead, and the ICM20948 can run in 6DOF mode.

## IMU Calibration

Some IMUs, such as the BMI270, BMI160, MPU9250, and MPU+QMC5883L, require manual calibration. This only needs to be performed once upon first setting up your SlimeVR tracker, however, you may need to perform the calibration multiple times before reaching satisfactory results. More information on how you would calibrate your IMUs can be [found here.](../server/imu-calibration.md)

---
### Credits
*Created by smeltie, edited by calliepepper and nwbx01*

A big thanks to everyone who took the time to fill out the survey.
