# Final Project: Robot Applications

## Table of Contents

- [Timeline](#timeline)
- [Class Community Guidelines](#class-community-guidelines)
- [Summary](#summary)
- [Team Assignments](#team-assignments)
- [Core Requirements](#core-requirements)
- [Project Ideas](#project-ideas)
  - [GoPiGo3](#gopigo)
  - [Bebop](#bebop)
  - [evoarm](#evoarm)
  - [turtlebot](#turtlebot)
  - [robot simulation](#robot-simulation)
- [Proposal](#proposal)
- [Working Prototype and Progress Report](#working-prototype-and-progress-report)
- [Project Demonstrations](#project-demonstrations)
- [Assessment](#assessment)
- [Receiving Assistance](#assistance)

## Timeline

Activity                                                                      | Deadline
----------------------------------------------------------------------------- | ------------------------------------------
Create a team and complete proposal (including any additional hardware needs) | by 4:20pm on Thursday, November 17th, 2022
Demonstrate progress during class work time (commits from each member)        | by 10:45am on Tuesday, November 22nd, 2022
Working prototype and complete progress report                                | by 4:20pm on Thursday, December 1st, 2022
Final demo and submission                                                     | by 9:30am on Tuesday, December 13th, 2022

## Class Community Guidelines

Throughout the completion of this project you must adhere to the [community guidelines](https://github.com/CMPSC-311-Allegheny-College-Fall-2022/course-information/blob/main/community_guidelines.md) that we developed as a class. To report any violations of the code of conduct, please submit an [anonymous form](https://forms.gle/tePfnLY12hyN1Xbd6). Students who think that the class should revise some aspect of the guidelines must use the GitHub issue tracker for that repository to suggest, discuss, and implement any required changes.

By working on and completing this assignment you agree to use the hardware given to you in a responsible manner. Each team is responsible for the safety and security of the robot while it is in your possession. You are allowed to take the robots used in this project outside of ALIC but you have to return all parts at the completion of this project, or if requested, at the end of the semester.

## Summary

This project assignment invites you to work in individually or in a team of two or three to implement a robot fulfilling a specific goal/task. Your project should design and implement a robotic system for some application of your choice using one of the robotic platforms used in this course. You could select to design and implement a multi-robot system, where more than one robot complete the goal/task, in which case it might be appropriate for two or more teams to collaborate.

## Team Assignments

You are invited to work in a self-selected team of two or three. Alternatively, you are also able to work individually. Once you have identified your team or that you prefer to work individually, please indicate it in the [team assignments](https://docs.google.com/spreadsheets/d/1167k-1ZGXR8TJqWdfp61kC7IDzhSVTUTHP7-Urx7ehc/edit?usp=sharing) spreadsheet so that we can ensure we have enough robots for everyone's preferences.

## Core Requirements

1. Your project must be approved by the instructor before you start working on it. The instructor will assess the viability of proposed projects after the lab session on November 17th and provide feedback via a review in GitHub Classroom pull request.
2. Your project must be developed for a specific application using a robotic system. You need to research the problem you select to get an idea of what has been already done. You must include references to existing work in your final report and justify why using your particular system is appropriate.
3. Your project must have an implementation component. You may write your code from scratch or reuse and extend some existing code. Obviously, anything you use that is not yours must be documented (in the source code and in the report).
4. Your project must be extensive enough to qualify as a project (think of an extension for one of the lab projects), but not too extensive so that you can not finish it by the deadline.

## Project Ideas

You are welcome to reuse existing code but you must either customize it or extend it. Taking existing code and just getting it to work does not constitute a project! Below are some ideas and resources, you are welcome to use your own search wizardry to find other helpful resources.

### gopigo

- [Dexter Industries sample projects](https://github.com/DexterInd/GoPiGo3/tree/master/Projects):

  - object avoidance robot
  - empathy bot
  - lane or object tracker
  - compass robot

- [ROS with gopigo](https://github.com/ros-gopigo3/gopigo3) (includes teleop). Another [ROS2 with gopigo reference](https://github.com/slowrunner/ROS2-GoPiGo3).

### bebop

- Search and rescue using drones. Can be implemented using pyparrot with Bebop drones and a search algorithm, such as A*.
- Product delivery to a specific location using drones and pyparrot library.
- Capture the flag using drones and AR Code reader. Can be implemented using pyparrot and [ar-markers library](https://github.com/pablodiegoss/pymarker).

### evoarm

- Tick Tac Toe, Towers of Hanoi, or other game using arm manipulation.
- Warehouse box manipulation.
- Drawing.
- [Alternate arm control](https://github.com/Atli-A/RobotWebControl)

### turtlebot

- [Various navigation strategies](https://github.com/turtlebot/turtlebot4_tutorials/tree/galactic/turtlebot4_python_tutorials/turtlebot4_python_tutorials) with [turtlebot 4 navigator](https://turtlebot.github.io/turtlebot4-user-manual/tutorials/navigation.html#turtlebot-4-navigator).
- Object recognition. See the bottom of [TurtlebotIsGo Unit](https://github.com/turtlebot/TurtleBot4Lessons/blob/main/units/Unit00-TB4-Introduction/L02-TurtleBotIsGo/U00-L02-TurtleBotIsGo.md) to see how to enable the camera in RViz.
- Multi-robot information exchange using ROS for some task, for example sending command from one turtlebot to another.

### Robot Simulation

- Implement an application task using a [Turtlebot 4 simulation](https://github.com/turtlebot/TurtleBot4Lessons/blob/main/units/Unit00-TB4-Introduction/L01-IgnitionBlastoff/U00-L01-IgnitionBlastoff.md).
- Implement an application task in [Gazebo](https://classic.gazebosim.org/tutorials).

## Proposal

You are invited to develop a project idea by the end of the lab session on November 17th. In the proposal document, please address all TODO tags that ask you to document your idea, outline acceptance criteria, illustrate its feasibility, and indicate whether additional hardware is needed. The instructor will provide feedback soon after proposal submission and may ask to adjust the proposed idea or its acceptance criteria.

## Working Prototype and Progress Report

During the lab session on Thursday, December 1st, each team will participate in demonstrating their working prototype. Prototype here means a functional but not a final version of a robotic system. This prototype should contain implementation of partial functionality of your project idea. This prototype should be ready to be demonstrated during the robotics community event. You are also responsible for complete a progress report document by the end of the lab session on December 1st.

## Project Demonstrations

At the beginning of the class session on Thursday, December 13th, each team will be given an opportunity to demonstrate their project. When the class session starts, teams will be given a few minutes to set up their demonstrations and get them running. Then, class members will participate in an interactive demonstration session, where everyone will be able to view each demonstration.

## Assessment

The grade that a student receives on this assignment will have the following components.

- **GitHub Actions CI Build Status [up to 5%]:**: For final project repository associated with this assignment students will receive a checkmark grade if their last before-the-deadline build passes.

- **Mastery of Verbal Explanation during the Demonstration [up to 15%]:**: Since the ability to communicate technical details of a project is crucial to building successful software and hardware applications, a portion of students' project grade will be determined based on the quality of the project demonstration during prototype and final demonstrations.

- **Mastery of Technical Writing [up to 25%]:**: Students will also receive a part of their grade when the responses to the writing prompts presented in the `report.md` reveal a proficiency of both writing skills and technical knowledge. To receive full points of this component, the submitted writing should have correct spelling, grammar, and punctuation in addition to following the rules of Markdown and providing complete and conceptually and technically accurate answers.

  - Please note that the "Check Spelling" GitHub Actions check may flag proper nouns or other real words if the dictionary it uses does not contain them. If your "Check Spelling" GitHub Actions check is failing due to a correctly spelled word being incorrectly flagged as "unknown" by CSpell, you will need to add the word to the list of words in `.github/cspell.json`.

- **Mastery of Technical Knowledge and Skills [up to 55%]**: Students will receive a portion of their assignment grade when their project design and implementation reveals that they have mastered all of the technical knowledge and skills developed during the completion of this project. Any written programs must be inside `src/` directory. As a part of this grade, the instructor will assess aspects of the project including, but not limited to, the appropriate design of the robot task, the completeness and correctness of the implemented software, effectiveness of experiments, the use of effective source code comments and Git commit messages, and satisfaction of the acceptance criteria set up by the team.

- **Continuous Progress [up to 40% deducted points]**: To ensure equal team effort and timely troubleshooting, students may lose up to 40% of points from their final deliverable for not demonstrating continuous team effort on this project. Each activity not submitted by the stated deadline in the [Timeline](#timeline) section by ALL team members will result in -10% unless the effected team member or the whole team (if the entire team was effected) can demonstrate circumstances beyond their control (e.g., illness, hardware challenges unsolvable in time, etc.).

All grades for this project will be reported through a student's gradebook GitHub repository.

### GatorGrade

You can check the baseline writing and commit requirements of this project by running department's assignment checking `gatorgrade` tool. To use `gatorgrade`, you first need to make sure you have Python installed. Then, you need to install `gatorgrade`:

- First, [install `pipx`](https://pypa.github.io/pipx/installation/)
- Then, install `gatorgrade` with `pipx install gatorgrade`

Finally, you can run `gatorgrade` to check baseline writing and commit requirements:

`gatorgrade --config config/gatorgrade.yml`

## Assistance

If you are having trouble completing any part of this project, then please talk with the course instructor during the laboratory session. Alternatively, you may ask questions in the Discord channel for this course. Finally, you can schedule a meeting during the course instructor's office hours.
