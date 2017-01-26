*****************************************************
ME 450 Project Requirements Spring 2017 - version #2
*****************************************************
The overarching goal of this project is to apply basic engineering knowledge to augment an autonomous baja ground vehicle platform so that it can be controlled autonomously using both steering and speed commands. The project can be broken up into two main tasks:

1) Design and Manufacture
2) Experimental Testing

These tasks will be Completed in Parallel
------------------------------------------
The idea is that during :ref:`expr` several of the students will become intimately familiar with current vehicle system by immediately beginning to :ref:`test_steering` as they set the stage for :ref:`test_speed` and simultaneously inform the :ref:`design`. 	The idea is that the students should coalesce to complete the entire project as a whole and everyone should be familiar with the different facets of the project as they cultivate and hone their engineering skills.

.. sidebar ::  Everyone should Be an Expert

	Once the team is organized after the initial design phase, the team should work together to assign responsibility to individuals for specific parts of the project. For instance, if the team was designing an `Automated Battery Exchange System For a Quadcopter <https://www.youtube.com/watch?v=LfD-oQ66o3U>`_, one guys would be the "gripper mechanism expert" another guy might be the "linear actuator expert" etc.

These two tasks are described in more detail below.

Meeting Schedule
------------------
As mentioned (via email on Jan 8th) the students are all responsible for these :ref:`meeting`. It is critical to complete these (weekly meeting notes) the team lead is responsible to manage the progress and tasks of the rest of the students and to create a Gannt chart to organize the overall project goals.

.. _design:

1) Design and Manufacture
##########################
Systems to control vehicle throttle and brake
**********************************************
In this task, students will be required to apply basic knowledge of electro-mechanical systems to remotely control the position of the vehicle throttle. In doing this task, students will have to:
	* Select appropriate actuators (i.e. step motor, linear actuator, rotor motor). Considerations will include torque and speed requirements (which are also to be determined), 	safety, reliability and cost.
	* A soft requirement is that the motors are back-drivable. This would be an extremely useful vehicle feature for the lab's research goals, but is not a hard requirement because it is a challenging task.

		* For those of you who do not know what back-drivability of a motor is check out `this video <https://www.youtube.com/watch?v=oAjfjU7yxoY>`_.

	* Determine actuator positions (after selecting one or more of the following; potentiometer, optical encoder, limit switch, etc.). Considerations for this task will include 	reliability, safety, and cost.
	* Design and manufacture (or purchase) brackets and mounts to support all of the devices 	used in both throttle and brake systems. A basic stress analysis on these systems should be 	performed and the entire system should be moderately resilient to the elements.


.. _expr:

2) Experimental Testing
########################

Develop computer code to control the vehicle using steering angle and longitudinal speed
*******************************************************************************************
In this task, the students will be responsible for developing a rudimentary control algorithm (i.e. PID controller) to ensure that the vehicle can track predefined control signals.

	* Design and manufacture (or purchase) any additional sensors and electrical equipment to accomplish this task.
	* NOTE: to a large degree this task has already been accomplished (at least for the steering system). It is however up to the students to become familiar with it and assess the system's reliability and make any needed repairs or replacements.

.. _test_steering:

Test Steering System
************************
	* Within the first month, students will become familiar with the current steering wheel actuator system and if needed replace any electronic or mechanical components.
	* An adequate series of tests will be subsequently designed and carried out

.. _test_speed:

Test Longitudinal Speed Systems
**********************************
	* As the **Design and Manufacturing** of these systems are carried out, the
	* Both the throttle and brake systems will be tested to ensure that the they can operate the 	vehicle controls as expected. To do this basic knowledge of control and coding will be applied.
  * An adequate series of tests will be subsequently designed and carried out

Remotely Control Vehicle
**************************
	* For safety, the first series of test where the vehicle is being controlled remotely and with basic PID controller will be performed with the vehicle on an elevated platform (i.e. with the 	tires off of the ground).
	* This is the next set of tests where the vehicle is controlled remotely as it navigates in a designated area.
	* This is the next set of tests where the vehicle is controlled using the PID controller as it navigates in a designated area.


Current Platform:
###################
The current vehicle has and actuator on the vehicle to control steering and there is station that is capable of teleoperating the vehicle using a steering wheel attached to an actuator for haptic feedback. However, there are significant dropouts in the control signals and the system is very rudimentary. Therefore, this project will be responsible for addressing these issues and creating a platform that has the mechanical and electrical components needed for autonomous and teleoperated driving.

.. image:: pics/plat.png
