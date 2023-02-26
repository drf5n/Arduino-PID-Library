***************************************************************
* Arduino PID Library - Version 1.2.2
* by David Forrest <drf5na@gmail.com>  2023-02-24
* by Brett Beauregard <br3ttb@gmail.com> brettbeauregard.com
*
* This Library is licensed under the MIT License
***************************************************************

 - For an ultra-detailed explanation of why the code is the way it is, please visit: 
   http://brettbeauregard.com/blog/2011/04/improving-the-beginners-pid-introduction/

 - For function documentation see:  http://playground.arduino.cc/Code/PIDLibrary


This fork uses back calculation per [Astrom 1989](http://cse.lab.imtlucca.it/~bemporad/teaching/controllodigitale/pdf/Astrom-ACC89.pdf) to manage integral windup. 

The back calculation should prevent integral windup be dynamically limiting the Intergrato to precent the Control Output
from exceeding the limits.  Large errors far outside of the proportional range (error > MaxOutput/kP) will produce MaxOutput and 
inhibit integral growth.

See   

*  https://github.com/br3ttb/Arduino-PID-Library/pull/116 -- Pull request to the PID_v1 library
*  https://github.com/br3ttb/Arduino-PID-Library/issues/76#issuecomment-1445273655

