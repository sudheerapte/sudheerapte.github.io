---
layout: post
title: Smart does not Mean AI
---

# We want smart machines. Does that mean "AI" machines?

_This series of articles tries to define what makes machines smart.
We use the example of "Sawyer", a smart industrial manufacturing robot
from Rethink Robotics, because I am most familiar with it, but the
principles are universal._

Thousands of clever researchers have been burning the midnight oil
toward the goal of human-like intelligence for over sixty years
now. Along the way, these researchers have been able to solve many
practical problems that require smarts. They have created algorithms
like "tree search" and "back propagation" that are useful in many
areas of computer science as well as in diverse practical applications.
Every few years, a breakthrough reaches the public and captures the
imagination, and a lot of hype about the term "AI" takes hold, fueled
by the business press. The hype raises hopes and fears about the
technology. After a few months, it becomes clear that the hopes and
fears were overblown, leading to disillusionment and loss of interest.
See [Rodney Brooks's blog
posts](https://rodneybrooks.com/forai-the-origins-of-artificial-intelligence/),
in which he tries to put the thing in context.

But, in the real world, what makes a "smart" machine?

Smart is what smart does, and it depends on the job.

## Collaborative Robots

Let's talk about smart robots as an example. To narrow the
description, we'll talk about robots that do something useful that
people will pay for: perhaps packing manufactured parts in an
industrial plant, or helping harvest a crop.

Most people using smart robots want them to be good employees: get the
job done without requiring the employer to put in much effort.  In
practice, there are two key sources of effort. The first is to train a
robot to perform a task. The second is to modify the workspace
environment to make the task fit seamlessly into the work line. For
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
presented in the exact same orientation every time. This, then, is a
third friction point.

So, a "smart" robot for this job is one that addresses each of the
above friction points. Going in reverse this time:

1. To address the brittleness of the task: the robot needs some
awareness of its surroundings to compensate for minor changes. Perhaps
it has built-in vision so that it can adapt to the orientation of the
parts as they come in. When holding the part, it should be able to
tell when it has dropped the part so it could try again or alert
someone.  When placing the part, it would be nice if it could sense
the force-feedback so that it can feel its way to the exact spot to
place the part. If someone nudges its work table, then the robot could
have the ability to re-orient itself using landmarks fixed to the
table so that it could continue to do the task.  This will make the
work less brittle.

2. To address the gripper integration: the robot needs a generic model
common to a wide variety of grippers, and grippers that are designed
for different kinds of parts, with a standardized mechanical
interface, electrical signaling conventions, and digital APIs
implemented at the robot's wrist. Then it will be simple for the
customer to attach a suitable gripper for the given task, and to
switch grippers for a new task.

3. To address the training time: the robot needs a high-level
programming capability, in which ordinary people (not engineers or
programmers) can use the robot's own arms and a visual user interface
to order and describe the logic to be followed by the robot. If the
co-workers themselves can train the robot, it will remove a major
source of friction.

The above points are addressed by so-called "collaborative robots" or
"cobots", of which the best example is Rethink Robotics's Sawyer.

![Sawyer pic](https://spectrum.ieee.org/image/MjYxMjM2MQ.jpeg)

Besides the above three sources of friction, there is another large
organizational barrier: if the robot is not safe around people, then
the people have to be cleared out of the area and safety cages need to
be built around the robots. This, too, has been addressed by these
cobots, as these robots are designed to be used around humans. If you
try to hold Sawyer's arm while it is performing a task, it will sense
the force and stop its task immediately. And, as you can see above, it
looks cute and harmless, too.

## It's About Product Design

If you read through these descriptions, you can see that the features
above that make Sawyer a "smart" robot have almost nothing to do with
"AI", and everything to do with a holistic product design that keeps
the use cases front and center.

It is not a surprise that a well-designed product sells.  What might
be more controversial is that what users call "smart" does not align
with what the latest buzz-words call "artificial intelligence".
