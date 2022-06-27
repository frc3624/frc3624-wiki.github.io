# Field Oriented Drive

Field Oriented Drive is a radically different driving style, and it is hard to explain solely through text. That's why I've included a helpful video made by yours truly, about how Field Oriented Driving works

<iframe
    width="640"
    height="480"
    src="<insert youtube link here>"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

## Script
If you'd like the loose script to read along with, I have it linked below. I didn't
use it verbatim, so take it for what it is

Hi, I'm Haadi, I'm one of the team captains for Team 3624, and I wanted to give
a brief overview of Field Oriented Driving, or FOD.


Field Oriented Drive is not a complicated topic, but a visual aid will help in
your understanding. This is critical for both Software and the Drive team. I
will talk about the impacts of FOD for both camps.


If you're a member of the software team, I would recommend to watch this entire
video, and if you're on Drive, you can skip to the timestamp I've probably
included, but it won't hurt to watch the whole thing.


First up, this grid represents the field of an FRC competition, minus most of
the bells and whistles of game elements. This stripped down grid will help us
understand what's really going on.


Alright, without any further adieu, here we go.


This blue square represents our robot, and these yellow lines I draw will represent
potential paths for the robot to travel. The front of the robot is denoted by
that little red mark on the front. A non FOD is what we're all the most
familiar with, it's more or less how a car works. 


Here's an example:


Say you're in a car, and you turn left. \*Draws\* . Now, the front of the car
is now pointing in the x direction, instead of the y. What this means now, if
you hit the accelerator, and you go "straight" in relation to the car, you're
now going left/right instead of the up/down you would have before.


Now, if you go and turn right, you'll be back in the same orientation you were
before. This should make sense, as we've all been in a car before. But for a
robot, this can be a bit confusing. Remember, when you're in a car, you're in
a first person POV. When you're directing a robot, most of the time, you're in
a 3rd person POV. This can be disorienting, because forward for the robot, does
not necessarily mean forward for the driver.


This is especially an issue when you have an obstruction in the field. Now say 
you're behind this obstruction, and you no longer can clearly see the robot. 
Now say, there's a robot blocking the camera you would normally be able to see
through. This causes a lot of troubles if you're trying to get out of there.


This is where FOD comes in.
Field Oriented Drive now sees this grid as an immutable property, meaning the
grid will never change. What this means, is that when you press forward on the
controller, it will ALWAYS move in the +y direction. When you go right, it will
ALWAYS move in the +x direction, and so on.


This is incredibly useful, since it drops a lot of the potential problems we'd
experience in the scenario I just described to you.
Alongside this, FOD is highly useful for swerve/mecanum drivebases.


Thank you for watching, and hopefully you understand what FOD is, and its
benefits.
