# Arduino-stepper-FBD
Arduino stepper control part using FBD for feeder project

The code is for a light duty parts feeder project.

The system includes a 300 LPI linear optical encoder and film for incremental quadrature (4X) feedback precision and a remote status LED with momentary push button switch. 

A clamp/brake may hold work at each stage if ~2 ft. lb. motor holding is insufficient. 

here are 6 sequential stages for a 200 step (1.8°) motor with GT2 belt and 20-tooth pulley.

Each stage is to a predetermined count stop. At each stop, the LED goes ON and, the motor, and if necessary, a mechanical clamp, securely holds the part in position. After stage work is complete, the hold clamp is released, the momentary switch is pressed, the LED goes OFF and the work moves to the next stage stop. 

The final stage returns the parts carriage to 0 to repeat the sequence.
