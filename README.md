# Arduino-stepper-FBD
Arduino stepper control part using FBD for feeder project

The code is for a light duty parts feeder project.

The system includes a 300 LPI linear optical encoder and film for incremental quadrature (4X) feedback precision and a remote status LED with momentary push button switch. 

A clamp/brake may hold work at each stage if ~2 ft. lb. motor holding is insufficient. 

here are 6 sequential stages for a 200 step (1.8°) motor with GT2 belt and 20-tooth pulley.

Each stage is to a predetermined count stop. At each stop, the LED goes ON and, the motor, and if necessary, a mechanical clamp, securely holds the part in position. After stage work is complete, the hold clamp is released, the momentary switch is pressed, the LED goes OFF and the work moves to the next stage stop. 

The final stage returns the parts carriage to 0 to repeat the sequence.

Status transition and control logic is implemented using FBD and FSM pattern. 

# Stages
- Stage 1: 0 to 2” travel (motor count = 600;)
- Stage 2: 2” to 24” travel (motor count = 7200;)
- Stage 3: 24” to 48” travel (motor count = 14488;)
- Stage 4: 48” to 72” travel (motor count = 21600;)
- Stage 5: 72” to 94” travel (motor count = 28288;)
- Stage 6: 94” to 0” travel (motor count = 0;) Return to 0

They can be added easily and configured. 

# Parts
- Arduino Uno
- Stepper Motor, NEMA23, 425oz/in, 1.4A/Series
- Motor Driver H-Bridge, L298N
- Push Button Momentary Switch, Remote
- LED, Remote
- Optical Linear Encoder, Dual Photo Interrupter, 300 LPI, 630-HEDS-9731-252
- Encoder Film, 300 LPI
- Belt, GT2
- Pulley, 20-Tooth

