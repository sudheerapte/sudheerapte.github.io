---
layout: post
title: Interaction Design, not UI Design
---

# Interaction Design, not UI Design

Interaction Design is about *behavior*: how the system or application
interacts with the user.

Usually, graphical output on a screen, and keyboard and mouse input,
are the primary means of interaction with a software application. The
field of Interaction Design is dominated by this format. Interaction
design gurus like Alan Cooper have devoted much thought to how the
application ought to capture the user's attention (application
"posture": sovereign, transient, daemonic, parasitic) and how
different design styles should be used in these cases.

But this focus is very limiting, particularly when considering
embedded systems.

The user of an embedded system is likely not sitting at a desk,
looking at a screen. Instead, they may be engaged in different
work-related activities where interaction with the system happens at
different times in different ways.

A graphical screen might not be present; even if there is one,
application output could include simpler visual indicators like lights
(LEDs), including combinations of colored lights that can blink in a
pattern or show animations. Also common are extremely limited LCD or
LED panels that can show (for example) only a few text characters
and/or a few predefined elements that can be on or off.

Beyond vision, two other senses are also usable for output to the
human user:

* *Sound:* beeps, chirps, alarms, and more complex synthesized output
  including musical notes and spoken words.
  
* *Touch*, Vibration of an element that is held in the hand or is
  otherwise next to the user's skin, and more complex haptic feedback
  through special-purpose devices worn on the hand.

Similarly, there is a wide variety of methods by which the user can
provide _inputs_ to the application through sensors. Mobile phones
already contain touch-sensitive screens, gyroscopes, and
accelerometers; industrial equipment can reuse a wide variety of
sensors that were originally developed for sensing phenomena in the
real world. For example, a motion sensor can detect when someone
crosses a threshold to a door, so that this user action becomes an
input to the application.

A smart embedded application can use all of these means of interaction
and produce intelligent behavior. Interaction design must include all
of these methods of input and output.
