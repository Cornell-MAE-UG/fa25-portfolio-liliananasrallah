---
layout: project
title: MAE 3780 Robot Competition
description: Design Project
technologies: Arduino, Fusion360, C++
image: /assets/images/robot.jpeg
--- 
## Cube Craze
The objective of this competition was to design a robot that would collect more 1 inch blocks than the other robots. The arena was a 4 by 3.5 foot yellow and blue board with a 3 inch black border and 20 cubes scattered in the middle third. The two competing robots start on opposite sides of the board, and whoever has the most blocks within the perimeter of their robot at the end of 60 seconds wins. We had a budget of $40 and the robot had to fit within a 8 by 8 inch box. 

<figure align="center">
  <img src="{{ '/assets/images/robot.jpeg' | relative_url }}"
       alt="photo of robot"
       width="500">
  <figcaption><strong>Figure 1.</strong> Our final robot design.</figcaption>
</figure>

## Robot Design and Strategy Overview
Overall we wanted to keep our robot design and strategy as simple as possible to limit the amount of issues that might arise. Our robot consists of the given chassis, a surrounding box enclosure with slots for our 3 QTI sensors, and a flap in the front. The flap ensures that the boxes can enter our robot perimeter, but cannot escape when driving backward or if we are getting pushed. We have used the small breadboard with the Arduino for wiring our motors and a larger breadboard for wiring our sensors. We used 3 QTI sensors located at the front left, front right, and center back of our robot. Ideally during the competition our robot will start at an angle and head to the center right of the board then turn and move across the board in one initial pass to collect as many blocks as possible. Then our robot will continue to move forward and turn right or left depending on whether the left or right QTI sensor detects the black border. The robot will drive forward when the back QTI sensor detects the border. When both the front QTI sensors detect the border the robot will stop.

## Competition Analysis
Our first round went terribly, we did not check the voltage of the battery we were given because in the rules it said that a new 9V battery would be given to us and so our robot did not start at all because the battery was dead. We rapidly switched batteries with a bit of a higher voltage but it still was not quite 9V and so for the next 2 rounds our robot was unable to turn and would only move forward very not smoothly. When we finally switched back to the battery we had originally used when testing our robot ran as intended because the voltage was indeed 9V. After this switch our robot successfully moved across the center of the board to collect blocks and would continue to drive around. We were pleasantly surprised with how the robot responded when in contact with the other robot. We thought our robot would be the one getting pushed, but our robot was actually robust enough to keep moving and eventually push the other robot out of the way. One thing that was not ideal, but not the end of the world, was that our two front QTI sensors would sometimes both sense black when only one was on black and thus stopping our robot. It would have been nice to keep driving around and potentially collect more blocks, but it was able to keep the initial blocks collected during our starting sequence in our robot perimeter. Also, if both robots headed to the same area of the board to collect blocks sometimes we would get unluckily turned around and not collect many blocks. 

## Conclusions
Overall, our robot performed very well once we found a working battery, and it operated how we intended it to. Our robot consistently collected about half the blocks, and did not drive off the board. As mentioned before, after our robot completes it first sweep, it continues driving around the board, adjusting when the border is detected to avoid driving off or getting pushed. When just the left QTI sensor is triggered the robot turns right, when just the right QTI is triggered the robot turns left, and when the back QTI is triggered the robot drives forward. When both front QTI sensors were triggered, we wanted to have the robot back up and turn around so it could continue driving around and collecting blocks. However we were having issues with getting this part of the code to work, so instead we had the robot just stop. If we redid this project, we would try to figure out how to make that part of the code work. We might try to use interrupts instead of while loops, and maybe even logic gates so there could be a separate arduino pin corresponding to the border being sensed in the front. Additionally, we would try to finalize our enclosure and flap design earlier so we would not waste money on hinges and laser cut parts that were not used (even though we did not have issues staying under budget). We would advise future students to check the voltage of their battery on competition day because we know several other teams were also given dead batteries.

## Personal Contributions
- Robot design and competition strategy brainstorming
- Assembling the robot chassis (motors, wheels, breadboard, arduino)
- Building the ciruits (H-brigdes, QTI sensors)
- Writing and debugging code 
- Mechanical integration of QTI sensors
- Testing and debugging robot for milestones and competition
- Final report (conclusion, circuit diagram, flowchart, code)


