---
layout: post
title: Embedded Systems for Software People
---

# Embedded Systems for Software People

So, you're trying to understand embedded systems.

If, like me, you are not an electrical engineer, then myriad types of
printed boards, manufactured chips, and integration technologies out
there will scramble your mind.  If you are not very familiar with
electronic circuits, then this article is for you.

You might have tried reading books and articles for "beginners". These
are targeted toward people who want to make things, and they quickly
get bogged down in details.  For a software person who wants to
understand embedded devices, most of these details are irrelevant.
Forget about transistors, UARTs, and half-adders. We're skipping all
these trees and zooming out to see the forest!

## Traditional Embedded Devices

A little bit of history.

Traditional embedded devices are very small, low-power electronic
systems whose whole purpose is a single application. The vast majority
of them do their work autonomously; all they need is some source of
power. Some examples:

- *Thermostat:* wakes up periodically to read a temperature
  sensor, and based on the reading, it turns on or off a heater.

- *Industrial alarm:* repeatedly samples pressure sensors and sends an
  alarm signal if the readings are outside some parameters.

- *Gas meter:* reads an ultrasonic sound transducer to find the volume
  of gas passing through a pipe. Periodically also updates a dial
  display to show that reading.

The key characteristics of these devices are:

- They are somehow situated in the real world, connected to it with
  inputs and outputs.

- Their correct operation depends on being able to execute their logic
  within a tight time bound related to the real-world phenomena they
  are concerned with.

Most of the logic in the above types of devices can be implemented
directly with circuits, without anything we would describe as a
"calculation" or "software".

A complete embedded "system" is typically composed of several bunches
of such circuits and devices, which might be produced by different
vendors, wired up into a functioning system for a particular
purpose. The difference between "embedded device" and "embedded
system" is in the eye of the beholder: a seller of transducers might
think of their product as a "system", but the buyer might think of it
as an "embedded device" that they put together with other pieces to
create a system.

## All About Circuits

An embedded system is a bunch of circuits, communicating with the
world. Here's all you need to know about these circuits:

- Some circuits are *analog* and can listen to real-world sensors that
  produce continuously varying voltages, or send out varying voltages
  that make things move or heat up in the real world.

- Others are *digital* and require their inputs to be only one of two
  voltages that stand for zero and one. The exact voltages are a
  matter of convention.

- Still others have both types of elements and can convert between the
  two types of information: analog to digital, or digital to
  analog. You also get circuits that just perform the conversion.

- Some circuits are *memory* banks, made of materials that form a
  fixed number of "memory cells" that can each store and retrieve a
  bit: a zero or a one. You can address a memory cell using digital
  bits represented as voltages on multiple input wires.

  - Some of these *memory* circuits use materials that can remember
  their data even after they are powered off (*persistent* memory),
  while others require a little power to remain on, otherwise they
  forget their bits.

  - Some memory circuits can overwrite their stored data with new
  data, whlie others can only be written to once, and read multiple
  times thereafter.

- Some circuits are digital *logic* circuits: they can take digital
  inputs and produce digital outputs, performing some calculations.

- Some circuits are *oscillators*, which produce a periodic signal at
  a predictable rate. Among other things, this kind of signal can be
  used to synchronize multiple other circuits as a common clock.

There are many other kinds of clever circuits, but you get the idea.

Most of the types of manufactured boards, chips, and packages
available today, and the finished systems that are built from these,
consist of many of the above types of circuits already wired to
communicate with each other.

The example devices like thermostats described above are truly
standalone; but similar simple devices can also be part of a larger
embedded system built for a special purpose.  Vendors of specialized
sensors and actuators pre-integrate them with circuits, so that system
integrators can build larger embedded systems using the inputs and
outputs of these circuits.

These systems are common in industrial process control and
manufacturing, for example. As costs for these devices have come down,
their components have migrated into consumer-visible applications: a
modern automobile has dozens of embedded systems containing thousands
of these circuits, depending on how you count them.

## Embedded Systems and Smart Devices

### Microprocessors and DSPs

We mentioned logic circuits above, which convert input signals to
output signals based on some calculations.  Microprocessors are a type
of these, with one difference.  The electronic logic in microprocessor
circuits is not specialized for performing any particular
calculations.  Instead, it implements a general-purpose "program
execution" logic: given a series of numeric instructions written in
attached memory circuits, the microprocessor can execute these
instructions one at a time.

Software people are very familiar with microprocessors because they
form CPUs in modern computers, so I don't need to describe them
further.  The point is that microprocessor circuits are also used in
embedded devices, where they originated.

A close cousin of the general-purpose digital microprocessor is a
digital signal processor (DSP), which samples analog signals, runs
specialized algorithms on the results, and converts them back to
analog form--- a critical component of many telecommunication systems
or any other embedded systems that need to process analog data in real
time, such as complex high-fidelity sensors. DSPs run special
instruction sets designed for operations like convolution, dot
product, polynomial evaluation, finite impulse response (FIR) filters,
and fast Fourier transform (FFT).  The DSP can execute many of these
mathematical operations simultaneously in a single instruction, making
execution time much faster and more predictable than a general-purpose
computer CPU.

### Microprocessors and Computers

Computers in the abstract have a rich history from mechanical abacuses
through purely conceptual drawings from the time of Ada Lovelace, but
they got a boost with the advent of microprocessors. If you consider a
modern microprocessor-based computer as a stage within the history of
embedded systems, then the computer is an aberration.  It turns the
concept of an embedded system on its head.

In a computer, the entire purpose of an embedded system has been
perverted to running abstract programs, instead of sensing and acting
upon the real world. Any communication with the outside world for a
computer is usually in service of the needs of the program.  You could
say that where its embedded ancestors have been extroverts, a computer
is an introvert.

To use a microprocessor, as you know, someone first needs to load a
program into memory and tell the microprocessor where the program
starts.  The "brain" in smart devices today is typically implemented
as software running inside a microprocessor.  This is where software
meets embedded devices.

Embedded systems developers found that they could modify and support
their products easily if they integrated their various component
circuits with microprocessors, so that their logic was expressed in
software. Software could be made more powerful, could be upgraded in
shipped systems, and even fixed or changed in the field.

### Microcontrollers and SoCs

Almost immediately after microprocessors were invented, manufacturers
produced a chip containing a microprocessor, some memory, and other
input/output peripheral circuits that are typically needed for a
microprocessor to function, to form a complete "microcontroller"
chip. (Such "integrated circuits" (ICs) are really many different
circuits by our definition, all manufactured together on a single
die.)

Cheap microcontrollers were a major innovation for the industry of
embedded systems. Not only could embedded systems developers build
their products more easily because memory and peripherals were already
integrated, but also, it allowed the sensor and actuator device
manufacturers to provide a built-in API to their devices in software,
by pre-integrating them with microcontrollers.

The entire supply chain underwent a transformation.  Embedded systems
developers could avoid costly, special-case hardware integration.
Instead, they could use standardized hardware interfaces to the
microcontrollers that came with component devices, and then use the
software API to integrate the sensors, actuators, and other
specialized circuits.

Increasing numbers of high-value embedded systems are becoming "smart"
as the microcontrollers get bigger and can hold more software.  At
least one microcontroller in the system can run a significant amount
of software and a user interface. An example is a modern digital
camera. Its distinctive features are its liquid-crystal display (LCD)
panel that shows a user interface, and accompanying dials and knobs
through which the user can browse and select options.

The inevitable result of Moore's Law, more and more powerful computers
could be built on a single chip, including not just memory and I/O,
but also other advanced components needed for a complete computer:
multiple processors, graphics processing units (GPU), Wi-Fi module,
bluetooth radio, standard USB, Ethernet, power management circuits,
and so forth.

Called a "System on a Chip" (SoC), these are complete computers with
greatly reduced power consumption and size, that can be crammed into a
mobile phone with plenty of room for a battery. The ones used in
mobile phones, of course, also include an accelerometer, a GPS, and a
cellular modem.
