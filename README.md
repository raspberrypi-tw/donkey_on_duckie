# Running Donkey Car on Duckie Bot using Adafruit DC Motor HAt

* [Donkey Car Project](https://github.com/autorope/donkeycar)
* [Duckietown Project](https://github.com/duckietown/Software)
* [Adafruit DC Motor HAT](https://www.adafruit.com/product/2348)

donkey car commit [ec7ea7a9d](https://github.com/autorope/donkeycar/commit/ec7ea7a9d7687ba5bb0d9daf4c8dc23f75549d03)

## Install

1. install Adafruit-Motor-HAT-Python-Library
   ```bash
   cd Adafruit-Motor-HAT-Python-Library
   python3 setup.py install
   ```

2. Install SONY PS3 Joystick Controller
    ```bash
    git clone https://github.com/raspberrypi-tw/donkeypart_ps3_controller
    cp part.py donkeypart_ps3_controller/donkeypart_ps3_controller
    cd donkeypart_ps3_controller
    python3 setup.py install
    ```

3. Copy actuator.py to donkeycar source path
    ```bash
    cp actuator.py ~/donkeycar/donkeycar/parts
    ```

4. Re-install Donkey Car
    ```bash
    cd ~/donkeycar
    pip3 install -e .[pi]
    ```

5. Modify myconfig in ~/mycar
   from
   ```
   # DRIVE_TRAIN_TYPE = "SERVO_ESC" # SERVO_ESC|DC_STEER_THROTTLE|DC_TWO_WHEEL|SERVO_HBRIDGE_PWM
   ```
   to
   ```
   DRIVE_TRAIN_TYPE = "DC_TWO_WHEEL" # SERVO_ESC|DC_STEER_THROTTLE|DC_TWO_WHEEL|SERVO_HBRIDGE_PWM
   ```

