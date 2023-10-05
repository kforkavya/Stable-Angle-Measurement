## Kalman Filter Program Explanation

### Libraries:
- **Wire.h**: This library allows communication with I2C devices.

### Variables:
- **Gyroscope and Accelerometer Data**: `RateRoll`, `RatePitch`, and `RateYaw` store raw gyroscope data, while `AccX`, `AccY`, and `AccZ` store raw accelerometer data.
- **Calibration Variables**: `RateCalibrationRoll`, `RateCalibrationPitch`, and `RateCalibrationYaw` store gyroscope calibration values, and `RateCalibrationNumber` is used in the calibration loop.
- **Filtered Angle Variables**: `KalmanAngleRoll` and `KalmanAnglePitch` store the filtered roll and pitch angles, respectively. `KalmanUncertaintyAngleRoll` and `KalmanUncertaintyAnglePitch` store the corresponding uncertainties.
- **Filter Output Array**: `Kalman1DOutput` is an array used to store the output of the Kalman filter function.

### Functions:

1. **`kalman_1d()`**: This function implements a 1D Kalman filter. It takes the current state, uncertainty, input, and measurement as inputs and updates the state and uncertainty based on the Kalman filter equations. The filtered state and uncertainty are stored in the `Kalman1DOutput` array.

2. **`gyro_signals()`**: This function reads raw gyroscope and accelerometer data from the MPU6050 sensor using I2C communication. It calculates the roll and pitch angles using accelerometer data and updates the `RateRoll`, `RatePitch`, `RateYaw`, `AccX`, `AccY`, and `AccZ` variables.

3. **`setup()`**: This function is called once at the beginning of the program. It initializes communication with the sensor, calibrates the gyroscope by averaging raw values over a certain number of iterations, and sets up the serial communication for debugging.

4. **`loop()`**: This function is called repeatedly in the main program loop. It reads sensor data, subtracts calibration values, applies the Kalman filter, and prints the filtered roll and pitch angles to the serial monitor. It also contains a delay to control the loop execution time.
