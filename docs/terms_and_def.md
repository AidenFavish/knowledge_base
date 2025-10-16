# Terms and Definitions
Some simple relevant definitions for some terms you might see a lot of.

1. **ESC**: Stands for electronic speed controller. The flight controller sends signals to this component and the esc sends power to the motors accordingly.

2. **Serial Protocol**: A protocol to send data over one or a few wires. On linux its typically prefixed with ttyACM.

3. **USB**: A type of serial protocol (your probably already familiar with this).

4. **UART**: Also a serial protocol, consists of 4 wires, 2 for signal, 1 power, and 1 ground.

5. **UDP**: A very fast <u>network</u> protocol meant for streaming data that prioritizes speed over reliability (does not do robust packet loss checking).

6. **TCP**: Also a network protocol that you can send data with thats a bit slower than UDP but checks for packet loss and is more reliable.

7. **SITL**: Stands for *Software in the Loop* and is a way to simulate something using software (as opposed to hardware in the loop which typically simulates on device hardware).

8. **ELRS**: The protocol our controller uses to communicate with the drone. Very capable but we typically use low bandwidth (only stick movement and switches on controller).

9. **Baud Rate**: Describes the speed of data transfer over a wire. You see this when making serial connections. Typically over usb radio is 57600 and for direct serial connection 115200.

10. **RTK**: A gps device that sits on the ground and communicates with the drone via the ground station to enhance its position estimate.

11. **Telemetry Radio**: A radio that is connected to the flight controller that typically sends MAVLink messages to our ground station which are higher bandwidth and more powerful.

12. **MAVLink**: A standard message protocol that can communicate with our Ardupilot flight controller.

13. **GCS**: Stands for *Ground Control Station* and typically consists of a laptop (our Toughbook), the RTK and a telemetry radio.

14. **ArduPilot**: The firmware that runs on our flight controller. It maintains all the control loops and allows us to send only MAVLink commands to control it.

15. **EKF**: Stands for *Extended Kalman Filter* and is a standard sensor fusion algorithm. In the context of ArduPilot, this typically stands for the EKF that maintains the <u>position estimate</u> by fusing the following sensors: the gyroscopes (very fast polling but prone to drift), the gps (slower polling but quite precise), and optionally an RTK station (to enhance the estimate).
