555-EFI
=======

An electronic fuel injection system for the Rover 3.5L V8 engine based off a 555 timer

=======

I think an Electronic Fuel Injection system based off of the 555 timer would be something special. Below are my thoughts on possibly the most basic injection system I could come up based on the 555 timer.

There are three things I can think of that would be needed:

- A crank sensor can be used to tell the injection system when to fire the injector.
- An O2 sensor on the exhaust so you know what the average combustion is like. The value from the O2 sensor tells you if the air-fuel mixture is lean or rich.
- Potentiometer on the throttle so you can know the throttle position and the rate of change of throttle position.

The fuel pump supplies petrol to the injector rails at 40psi. You know that at this pressure, a certain pulse width will inject a known amount of fuel into the intake. The greater the pulse width, the more fuel is injected, and so the small the pulse width, the less fuel is injected.

A four stroke engine takes four  complete 4 stroke cycle takes two revolutions of the crank. Because of this, a crank sensor can be used to tell the injection system when to fire the injector. A flipflop/counter could be used to alternatly fire each bank of injectors in turn to make the system slightly more accurate? Or to keep it even more simple, the flipflop/counter could be used to fire the injectors, then count two revolutions, fire the injectors... etc

We know how rich/lean the mixture is by the reading from the O2 sensor and it will tell us if the mixture is lean or rich. If the mixture is lean then the engine needs more fuel, so the system would increase the pulse width. The opposite would occur if the mixture was rich.

If you suddenly open the throttle very quickly then the mixture is going to become very lean very quickly as air is rushing in and the system has not had time to richen the mixture. So the rate of change of throttle position can be used to signal the system to squirt more fuel in and richen the mixture for the sudden acceleration. On the other hand if you close the throttle to return the engine to idle, then the system has not had time to reduce the amount of fuel going in and so the mixture will suddenly be very rich and the engine will be wasting fuel.

In all, the system is trying its damn hardest all the time to get the 'perfect' O2 reading by constantly adjusting the amount of fuel injected.

The system could be improved by adding another O2 sensor. If there was one sensor per bank of cylinders, then the O2 readings would be more accurate as they would be an average of 4 instead of an average of 8. By using two 555 timers one can be used on each bank. Another way of improving the injection system would be to utilise more sensors that are already used in my Rover V8 3.5L engine. Sensors such as CTS (Coolant Temperature Sensor) and IAT (Inlet Air Temperature) would allow the engine to be slightly more efficient as the system knows the temperature of the engine, and the temperature of the air coming into the engine and can adjust the fuel injection accordingly.
