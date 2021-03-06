# Thermostatic chamber

This is student project of thermostatic chamber. This system was desgined to keep reference temperature.To build this project 
there were used elements like: chamber which keep temperature, SSR , temperature sensor, buttons, LCD and STM32F411RE.
![Photo of circuit](uklad.jpg "Photo of circuit")
Temperature was controlled by PID controller. Heater was controlled by PWM
signal. All things were programmed in STM32CubeIDE. GUI was done
in [TelemetryViewer](http://www.farrellf.com/TelemetryViewer/).
Project was composed of two stages. 

## Modeling
In this stage were done measurements which helped recognize the nature of object. The chamber was
testing by turning on the heater for some period of time and waiting for reaction of object.
Collected data let to start modeling and simulating in MATLAB. Object was recognize as
inertial element with a delay. This knowledge let use Matlab's cftool to find parameters. Next step was
simulation in Matlab's tool Simulink. 
## Testing 
Next stage was testing hardware and software. As i said, heater was 
controlled by PWM signal. To do that it was used algorithm of PID controller which
calculated a control signal interpreted as voltage. This control signal was
converted to width of PWM signal. That let to apply mains voltage for calculated period of time.
## How it works?
[Link for presentation](https://youtu.be/v-I5uuCyCsk)

## Conclusions
In this project it was used heater with power 2000 W and chamber with dimensions 345mm x 240 mm x 300 mm. These facts caused
that the PWM period had to last 1 second. Another thing was that the parameters of
PID controller from simulation had to be changed. That helped to better control the object. So the first
conclusion is that the power of the heater should be 
well chosen for volume of chamber. That can make easier controlling the object. Another thing is that to
improve the dynamics of the object is good to use some fan.
