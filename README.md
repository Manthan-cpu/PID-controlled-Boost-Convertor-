# PID-controlled-Boost-Convertor-
This project implements a closed-loop Boost Converter controlled by a Proportional-Integral-Derivative (PID) controller, designed and simulated using MATLAB Simulink, with real-time control executed via an Arduino microcontroller. 
A boost converter is a type of DC-DC converter that steps up a lower input voltage to a higher output voltage. In this setup, a PID control algorithm is used to regulate the output voltage of the converter to a desired setpoint, even in the presence of load or input variations.

The system is modeled and simulated in MATLAB Simulink, where the PID controller parameters are tuned for optimal performance. Using Simulink Support Package for Arduino, the model is deployed on an Arduino Uno, which handles real-time PWM control of the switching MOSFET in the boost converter.

Key Components:
Hardware:

Arduino Uno

Inductor, Diode, Capacitor (Boost Converter circuit)

N-channel MOSFET (e.g., IRF540N)

Voltage Divider (for feedback)

Load resistor

Software:

MATLAB Simulink

Simulink Support Package for Arduino Hardware

Working Principle:
The output voltage is measured via a voltage divider and read by the Arduino's ADC.

This feedback is compared to the reference voltage.

The error signal is passed to the PID controller, which calculates the control effort.

The Arduino uses this output to generate a PWM signal, which controls the duty cycle of the MOSFET.

The switching action adjusts the energy stored in the inductor, thus controlling the output voltage.

Objectives:
Maintain a stable output voltage regardless of variations in input voltage or load.

Demonstrate real-time hardware implementation of a Simulink-designed control system.

Explore tuning of PID parameters for fast and stable response.
