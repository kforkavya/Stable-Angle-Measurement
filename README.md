# Stable Angle Measurement

This is my self-project developed in March 2023, addressing critical challenges in angle measurements faced due to background turbulence and offset accumulation in gyroscopic sensors. The project focuses on achieving precise and reliable angle calculations even in the presence of these disturbances, using ARDUINO UNO and MPU-6050 (Gyroscope-cum-Accelerometer) ensuring accurate data for applications requiring stable orientation measurements.

## Challenges: Background Turbulence and Offset Accumulation

### Background Turbulence:
Background turbulence refers to continuous, low-intensity vibrations or movements in the environment where the sensor operates. These vibrations can be caused by various factors, such as nearby machinery, air circulation, or subtle surface movements. In the context of gyroscopic sensors, background turbulence introduces noise and disturbances in the sensor readings. Traditional sensors often struggle to distinguish between these external disturbances and actual motion, leading to inaccuracies in angle measurements.

### Offset Accumulation in Gyroscopes:
Gyroscopic sensors, over time, can develop an offset due to various factors, including sensor imperfections and wear and tear. This offset, often unnoticed initially, accumulates over time, causing a drift in the sensor readings. As a result, even when the sensor is at rest, it may indicate a non-zero rate of rotation. This offset accumulation is a significant challenge in applications requiring precise angle measurements, as it leads to incorrect orientation data.

## Key Features

- **Accurate Angle Calculation:** Implements sophisticated algorithms to filter out noise caused by background turbulence and corrects for offset accumulation, ensuring precise angle measurements.
- **Kalman Filtering:** Utilizes a Kalman Filter in Arduino IDE, a powerful tool for sensor fusion, noise reduction, and stabilization. The filter intelligently separates the genuine motion data from the undesired noise and disturbances, resulting in stable and accurate angle readings.
- **Real-time Monitoring:** Provides real-time angle monitoring through the serial monitor, enabling users to observe stable measurements and evaluate the system's performance.

## Technologies Used

- **Hardware:** Arduino UNO, MPU-6050 Gyroscope-cum-Accelerometer Sensor.
- **Software:** Arduino IDE.

## How it Works

Stable Angle Measurement utilizes the MPU-6050 sensor to capture gyroscope and accelerometer data. By employing a Kalman Filter algorithm in Arduino IDE, the project processes the raw sensor data. The filter distinguishes between actual motion data and disturbances caused by background turbulence. Additionally, it corrects for offset accumulation in the gyroscopic sensor readings. The resulting stable angle measurements are then available for real-time monitoring and various applications requiring accurate orientation data.

## Usage

1. **Setup Arduino IDE:** Open the project in Arduino IDE and upload it to the Arduino UNO board.
2. **Connect the Sensor:** Wire the MPU-6050 sensor to the Arduino UNO board according to the provided instructions.
3. **Run the Program:** Power up the system and observe stable angle measurements displayed on the serial monitor in real time.

## Contributions

Contributions and feedback are encouraged! If you have suggestions, bug reports, or improvements, please open an issue or submit a pull request.

**Stable Angle Measurement** - *Achieving Stability Amidst Turbulence. Developed by [Kavya]*
