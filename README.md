# LeptonGimbal
(Lepton 3.x made by FLIR)
Gimbal for thermal cam(geared motor type)

*BEFORE YOU CONNECT SERVO-SG90 YOU NEED TO CALIBRATION OFFSET WITH GY-521(MPU6050).

the original is as follows;-
https://www.instructables.com/Gyro-Stabilizer-W-Arduino-and-Servo/
name has been changed as LEPTONGIMBAL
limitation added for pitch and roll as follows;-

    // flush buffer to prevent overflow
    mpu.resetFIFO();
    if (-45 < mpuPitch && mpuPitch < 45) // range +/- 45 dgree
    Servo1.write(mpuPitch + 90);//mpuPitch opposite (90-mpuPitch)
    mpuRoll = mpuRoll - 6;                               //mpuRoll - 6 Vertical Adustment
    if (-45 < mpuRoll && mpuRoll < 45) // range +/- 45 dgree
    Servo2.write(90-mpuRoll);//(mpuRoll + 90)
    //delay(10);

    // flush buffer to prevent overflow
    mpu.resetFIFO();
This code is placed under the MIT License (MIT)    
