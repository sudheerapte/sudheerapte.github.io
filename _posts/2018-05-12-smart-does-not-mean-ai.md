---
layout: post
title: Smart does not Mean AI
---

# We want smart machines. Does that mean "AI" machines?

_This post is in progress. The first half is done. Text needs citations
and pics._

There's a lot of hype about the term "AI". Lately the term has come to
mean pattern recognition through neural networks of various
kinds. This is an old idea that has fundamentally not changed, just
become more practical because of high-speed computers. (See Rodney
Brooks's blog post on this topic).

There have been no dearth of tools in the arsenal of roboticists for
solving problems that require smarts. The humble "search" can be a
powerful way to solve problems. All of these algorithms are tools; but
in the real world, what makes a "smart" machine?

Let's talk about smart robots as an example. To narrow the
description, we'll talk about robots that do something useful that
people will pay for: perhaps packing manufactured parts in an
industrial plant, or helping harvest a crop.

Smart is what smart does, and it depends on the job.

Most people using smart robots want them to be good employees: get the
job done without requiring the employer to put in much effort.  In
practice, there are two key sources of effort. The first is to train a
robot to perform a task. The second is to modify the workspace
environment to make the task fit seamlessly into the work line: for
example, our part-packing robot, once it is trained to pick up a part
of a certain shape and place it into a box, needs to be fed the parts
in a predictable location and orientation every time, and also
repeatedly presented with boxes into which it can place the parts.

So, a smart robot would be one that reduces the effort in these two
areas. Brooks calls these "friction points". How hard are these? They
are real hurdles.

Today, the vast majority of robots require an engineer many days or
weeks to program a robot to do a given task. And, in order to modify
the environment and outfit the robot with a custom gripper to hold the
parts correctly, plus programming the robot to control the gripper,
can take anywhere from a day to many weeks depending on how much
custom work is needed. At the end of this "integration" process, the
robot can start doing the work, but its programming is still brittle,
prone to stoppage if a part arrives upside-down or a box is not
presented in the exact same orientation every time.

So, a "smart" robot for this job is one that addresses each of the
above points. Going in reverse this time:

1. To address the brittleness of the task: the robot needs some
awareness of its surroundings to compensate for minor changes. Perhaps
it has force-feedback sensing so that it can feel its way to the exact
spot to place the part, or built-in vision sensing so that it can
adapt to the orientation of the part. If the robot moves a little with
respect to its work space, then the robot could have the ability to
re-orient itself using fixed landmarks so that it could continue to do
the task.  This will make the work less brittle.

2. To address the gripper integration: the robot needs a generic model
common to a wide variety of grippers, and grippers that are designed
for different kinds of parts, with a standardized mechanical
interface, electrical signaling conventions, and digital APIs
implemented at the robot's wrist. Then it will be simple for the
customer to attach a suitable gripper for the given task.

3. To address the training time: the robot needs a high-level
programming capability, in which ordinary people (not engineers or
programmers) can use the robot's own arms and a visual user interface
to order and describe the logic to be followed by the robot. If the
co-workers themselves can train the robot, it will remove a major
source of friction.

The above points are addressed by so-called "collaborative robots" or
"cobots", of which the best example is Rethink Robotics's Sawyer.

