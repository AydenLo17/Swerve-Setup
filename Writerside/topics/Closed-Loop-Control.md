# Closed Loop Control

Closed-loop control typically refers to control of a motor that relies on sensor data to adjust based on error. Systems/mechanisms that rely on maintaining a certain position or velocity achieve this state using closed-loop control. This is achieved by feedback (PID) and feedforward control. Closed-loop control can be performed on the robot controller or on the individual motor controllers. The benefits of onboard closed-loop control are that there is no sensor latency, and the closed-loop controller has a 1 kHz update frequency. This can result in a more responsive output compared to running the closed-loop on the robot controller.

### Manual tuning typically follows this process:

1. Set all gains to zero.

2. Determine <math>K_g</math> if using an elevator or arm.

3. Select the appropriate Static Feedforward Sign for your closed-loop type.

4. Increase <math>K_s</math> until just before the motor moves.

5. If using velocity setpoints, increase <math>K_v</math> until the output velocity closely matches the velocity setpoints.

6. Increase <math>K_p</math> until the output starts to oscillate around the setpoint.

7. Increase <math>K_d</math> as much as possible without introducing jittering to the response.
<math> </math>