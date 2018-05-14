---
layout: post
title: Smart does not Mean AI
---

# We want smart machines. Does that mean "AI" machines?

_This series of articles tries to define what makes machines smart.
We use the example of "Sawyer", a smart industrial manufacturing robot
from Rethink Robotics, because I am most familiar with it, but the
principles are universal._

We will discuss later in this post what "artificial intelligence"
means in the popular press today. But, in the real world, what makes
a "smart" machine?

Smart is what smart does, and it depends on the job.

## Collaborative Robots

Let's talk about smart robots as an example. To narrow the
description, we'll talk about robots that do something useful that
people will pay for: perhaps packing manufactured parts in an
industrial plant, which is a task that Rethink Robotics's Sawyer robot
can be trained to do.

![Sawyer pic](https://spectrum.ieee.org/image/MjYxMjM2MQ.jpeg)

Most people using smart robots want them to be good employees: get the
job done without requiring the employer to put in much effort.  In
practice, there are two key obstacles. The first is to train a robot
to perform a task. The second is to modify the workspace environment
to make the task fit seamlessly into the work line. For example, our
Sawyer robot, once it is trained to pick up a part of a certain shape
and place it into a box, needs to be fed the parts in a predictable
location and orientation every time, and also repeatedly presented
with boxes into which it can place the parts. The boxes need to be
taken away when they become full.

So, a smart robot would be one that reduces the effort to overcome
these two obstacles. Rethink Robotics founder Rodney Brooks calls
these "friction points". How bad are these?

Today, the vast majority of robots (but not Sawyer) require an
engineer many days or weeks to program a robot to do a given
task. And, in order to modify the environment and outfit the robot
with a custom gripper to hold the parts correctly, plus programming
the robot to control the gripper, can take anywhere from a day to many
weeks depending on how much custom work is needed. At the end of this
"integration" process, the robot can start doing the work, but its
programming is still brittle, prone to stoppage if a part arrives
upside-down or a box is not presented in the exact same orientation
every time. This, then, is a third friction point.

Sawyer is "smart" for this job in how it addresses each of the above
friction points. Going in reverse this time:

1. To address the brittleness of the task: Sawyer has some awareness
of its surroundings to compensate for minor changes. It uses a
built-in video camera to look at incoming parts and can adapt to their
orientation.  When holding the part, it can tell when it has dropped
the part so it can try again or alert someone if it fails again.  When
placing the part into a tight space, it can sense the force feedback
and feel its way to the exact spot to place the part. If someone moves
its work table, then the robot can re-orient itself using
specially-marked landmark stickers affixed to the table.

2. To address the gripper integration: the robot maintains a generic
model common to a wide variety of grippers. Different companies can
design grippers for holding different kinds of parts, using moving
finger-like appendages, or vacuum suction cups, or any other
technology. As long as they conform to a standardized mechanical
interface, electrical signaling conventions, and digital APIs
implemented at the robot's wrist, then these grippers will "click"
into place on the robot. It will be simple for the customer to attach
a suitable gripper for the given task, and to switch grippers for a
new task.

3. To address the training time: the robot has a high-level
programming capability, in which ordinary people (not engineers or
programmers) can use the robot's own arms and a graphical user
interface to order and describe the logic to be followed by the robot.
Since the co-workers themselves can train the robot, they don't need
to wait for an expert engineer.

Besides the above three sources of friction, there is another large
organizational barrier: if the robot is not safe around people, then
the people have to be cleared out of the area and safety cages need to
be built around the robots. This, too, has been addressed by these
"collaborative" robots, designed to be used around humans, of which
Sawyer is an example. If you try to hold Sawyer's arm while it is
performing a task, it will sense the force and stop its task
immediately. And, as you can see above, it looks cute and harmless,
too.

## It's About Product Design

The features described above that make Sawyer a "smart" robot have
almost nothing to do with "AI", and everything to do with a holistic
product design that keeps the use cases front and center.

It is not a surprise that a well-designed product sells.  What might
be more controversial is that what users call "smart" does not align
with what the latest buzz-words call "artificial intelligence".

### A Note About "Artificial Intelligence"

Thousands of clever researchers have been burning the midnight oil
toward the goal of human-like intelligence for over seventy years
now. Along the way, these researchers have been able to solve many
practical problems that require smarts. They have created algorithms
like "tree search" and "back propagation" that are useful in many
areas of computer science as well as in diverse practical
applications.  Every few years, a breakthrough reaches the public and
captures the imagination, and a lot of hype about the term "AI" takes
hold, fueled by the business press. The hype raises hopes and fears
about the technology. After a few months, it becomes clear that the
hopes and fears were overblown, leading to disillusionment and loss of
interest.

Artificial Intelligence is suffering through one of these cycles
right now.  See [Rodney Brooks's blog
posts](https://rodneybrooks.com/forai-the-origins-of-artificial-intelligence/),
in which he tries to put the thing in context.

Today, the term essentially means machine learning algorithms like the
ones used to build game-playing, or speech-recognizing, or
pattern-matching systems to solve particular problems. If you really
want to learn what machine learning means, please read the post
["machine learning
explained"](https://rodneybrooks.com/forai-machine-learning-explained/)
by, yes, the same Rodney Brooks.
