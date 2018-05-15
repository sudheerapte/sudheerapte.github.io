---
layout: post
title: Building Smart Devices
---

# Building Smart Devices

The business of building embedded products is undergoing a sea-change
as software-intensive "smart" devices come into fashion.

With the push to add more and more hardware/software combination
devices that need smarts, particularly if they need a modern user
interface, embedded applications need more and more powerful
microprocessors with more memory and CPUs.

Buying microprocessors for building these products is the easy part;
staffing the projects is hard.  Companies already struggle to find
application programmers to build the logic for server- or
desktop-level computers; to find engineers who are both savvy enough
to work with embedded systems and also have the programming experience
to build moderate-sized applications is even harder. Software product
development teams containing programmers, designers, and SQA testers
need to be engaged on the development effort, even if they have not
worked on embedded systems before. This means making the environment
as familiar to them as possible.

## Choosing the Hardware Platform

Embedded hardware platforms are circuits built for low power use,
small spaces, and real-time integration with sensors and out-bound
signalling.  Depending on the sensing, networking, signalling, and
actuation features needed for a new product, a sub-set of the
available platforms is dictated.

Within these limited choices, the criteria for choosing a hardware
platform include:

- The CPU processing capacity and memory for running the application
  logic, and
- the availability of development tooling.

It seems inevitable that many companies will choose Linux-based SoCs
to base their "smart" hardware/software products on. Not only is there
a large community of experts and toolchains for developing and
delivering products on Linux, but also, with prices dropping for
system-on-a-chip platforms, there seem to be very few competitive
options.

## Enhancing Application Development Tools

Iterative product development needs continuous integration, daily
builds, and automated tests. The only practical way to get those with
hardware targets is to use software emulation. This is another
advantage of Linux: cross-compilation tools are well-known in the
Linux ecosystem, although they still need enhancements. To become
productive, these teams need development tools that enable a quick
turnaround from design to test.

## Developing User Interfaces

A large part of what makes devices "smart" is their interactions with
the user. People today have been trained to expect ease of use on
their mobile devices and computer games. To stay competitive, smart
embedded devices, if they have a user interface, must have one that is
well-designed.

User interfaces are notoriously slow to develop. Requirements changes
tend to crop up toward the end of the project, when early users or
beta testers get their hands on the user interface for the first
time. The underlying application model of a new product, and its
implications, are often exposed for the first time when people are
able to interact with the user interface. The result is often a period
of design churn just when the project managers thought the development
period was over. This can be a jarring change for embedded development
projects. Managers expect a period of extensive testing and bug fixes,
but not major design changes late in the game.

Iterative development methods can mitigate this problem, but in any
case, many changes need to be made to the code as the customer use
cases are better understood, or a better user experience is designed.

Traditionally, embedded systems tend to have minimal or nonexistent
UIs, so the involvement of User Experience (UX) designers and UI
developers brings a completely new dynamic to the project. Today the
most advanced user interfaces, outside of gaming, tend to be
web-based, and these tend to live most comfortably in cloud-based
software. Much of the tooling and culture is adapted to a cloud-based
environment. Engaging a team of web-UI coders on an embedded project
will require some work.

## Evolution of the Landscape for Smart Devices

All of the above changes can be managed; the result will be a changed
landscape for smart device development, with new tooling, application
architectures, and teams with experience working in this new area.

The relentless drive for efficiency will also change the architecture,
tooling, and teams. Today, to create smart devices, the embedded and
application teams are often managed separately; they are sometimes
actually physically separated, creating what are essentially separate
sub-products that are integrated to build the final product. This will
have to change.

Of course, many smart devices have cloud or server-side application
components with their own development teams already; but we're talking
specifically about the software that runs on the device itself.

