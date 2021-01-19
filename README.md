This software simulates the rocket system launch process. It is built to support the research process of Rocket Launch Control System.

# Introduction to the Rocket Launch System that this software simulates.
The rocket system can have up to 8 pad units, each unit can launch up to 2 rockets and each rocket has 2 relays. For example, if the rocket system has 4 pad units, then it can launch up to 8 rockets. There is a launch controller in the system to command to individual pad unit to launch rockets. In order to launch a rocket, the rocket owner places the rocket on the pad unit to connect the pad-unit’s ignition to the ignitor in the rocket. The owner can press a button on the pad unit to send an activation signal to the controller. When the controller gets the pad activated signal, the Launch Control Officer (LCO) can press an armed button on the controller sending a pad armed signal to pad unit to close the first of two relays. However, if the controller does not receive any signals from LCO in 10 seconds after receiving the pad activated signal, the rocket will be reset to original state. After the pad unit is ready to launch and the owner is back to a safe place, the LCO presses a rocket launch button on the controller. This button causes a second relay to close providing current to the ignition system in the rocket causing the rocket to launch. After the launching of the rocket succeeded, the rocket is reset to original state. When the pad is ready to launch, if the LCO pressed an armed button, the rocket will be reset to original state.

![alt text](https://github.com/An-Nguyen-profile-umn/Rocket-launch-research-project/blob/master/Launch%20logic.png)

Launch logic of a rocket

Note: In the software, "Control Button State: Launch" does not appear. Instead, the "Control Button State: Inactive" appears because the rocket state is reset immediately after launching successfully. Also, "Control Button State: Active" does not appear. Instead, the user will be asked to command "Reset" or "Armed Launch". If the user chooses "Armed Launch", "Control Button State: Launch Available" will appear. If the user chooses "Reset" or give no commands in 10 seconds, then the rocket is reset and "Control Button State: Inactive" will appear.

# Operating system problem:
This program is developed and ran well on Unix and Mac OS using IntelliJ. I use Java 9 to developed the program. For the purpose of demonstrating how the program works, I exported the program to an RocketLaunch.exe file. When running in Win 10 OS, the program has a "not a big duel" bug that does not happen when running in Unix or Mac OS. Generally, you will realize it when you run the program and the bug does not effect the correctness of the program. 

-The End-
