---
layout: post
title: Embedded Linux is Inevitable
---

# Building Smart Devices

With the push to add more and more hardware/software combination
devices that need smarts, particularly if they need a modern user
interface, applications need more and more powerful microprocessors
with more memory and CPUs.

Buying microprocessors for building these products is the easy part;
staffing the projects is hard.  Companies find it difficult enough to
find programmers to build the application logic for server- or
desktop-level targets; to find engineers savvy enough to work with
embedded systems and have the programming inclination to build
applications is even harder. Experienced software product development
teams containing programmers, designers, and SQA testers need to be
engaged on the development effort, even if they have not worked on
embedded systems before. This means making the environment as familiar
to them as possible.

## Linux Systems-on-a-Chip

It seems inevitable that many companies will choose Linux-based SoCs
for their "smart" hardware/software products. Not only is there a
large community of experts and toolchains for developing and
delivering products on Linux, but also, with prices dropping for
system-on-a-chip formats, there seem to be very few options.

Severe needs remain for development tools so that these teams can
engage and become productive. Product iterations need continuous
integration, daily builds, and automated tests. The only way to get
those with hardware targets is to use software emulation.

## The Problem with UIs

User interfaces are notoriously slow to develop. Requirements changes
tend to come up toward the end of the project, when early users or
beta testers get their hands on the user interface for the first
time. Iterative development is a way to mitigate this problem, but in
any case, many changes need to be made to the code as the customer use
cases are better understood, or a better user experience is designed.

Traditionally, embedded systems tend to have minimal or nonexistent
UIs, so the involvement of User Experience (UX) designers and UI
developers brings a completely new dynamic to it. Today the most
advanced user interfaces tend to be web-based, and these tend to live
most comfortably in cloud-based software.

So, engaging a team of web-UI coders on an embedded project is one
large change. But there is a second, more subtle difference when you
are building smart devices with easy-to-use UIs.

The key characteristic of embedded devices are that they are somehow
situated in the real world and must react to this world--- even at the
same time that a user is interacting with them. Depending on the
application and purpose of the smart device, this responsiveness is an
integral part of the product's user experience.

