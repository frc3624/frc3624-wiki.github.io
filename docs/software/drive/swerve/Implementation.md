# Implementation

## Design
This is probably **the** most important chapter for swerve. The question is, how on Earth do we pull this off? Well, it comes down to a clever design in the modules themselves. For a better, more thorough explanation, go to [this](../../../build/drive/Swerve.md), but the basics work as follows:
<br>

The module is built using a set of two main gears, one to spin the driving wheel along its treads (aka to move the robot translationally across the field), and another attached to the head of the wheel joint, enabling 360° rotation of the wheel. 

Think of this more or less as a glorified shopping cart wheel, there is complete freeness in this wheel in order to enable turning, but instead of it only being 2 wheels like this, it's all 4.

Cool, now how does this work? How can one drive motor possibly take care of translational motion, AND turning at the same time? The neat part, is that this isn't the solution, the solution is throwing more money at our problems. In order to take care of this problem, we just throw an extra motor per module (2x module, 8 for the whole drivebase) with one responsible for turning, and the other for translational motion.

Now, remember we're gonna want an encoder strapped in for the readouts of the angular velocity, as that's vital information, and we need it for any good PID control.

## Code

Now, this is going to be explained with actual code examples in a later chapter, but this section is still important. This is more focused on the underlying ideas and theories behind the code, rather than the code itself.

<Will work on this later it's a lot>
