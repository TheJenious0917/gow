---
layout: default
title: Overview
nav_order: 1
---
# Overview

<img width="100" src="{{ '/assets/img/gow-logo.png' | relative_url}}">
{: .float-left .p-3}

**Games on Whales (GOW)** lets you stream games (and GUI) running on Docker with HW acceleration and low latency.

The basic idea is that a [server](https://en.wikipedia.org/wiki/Server_(computing)) can stream games to clients the same way you play a video on Youtube. There are a lot of supported clients already such as: mobile phones, laptops, desktops, and even the Nintendo Switch! 

A server is not necessary a [gigantic beast of a machine](https://upload.wikimedia.org/wikipedia/commons/6/69/Wikimedia_Foundation_Servers-8055_35.jpg), it can be: a laptop, a normal desktop machine, or even something smaller and compact like a Raspberry PI ([in theory](https://github.com/games-on-whales/gow/issues/20)). Generally, you should be able to pick any OS that supports [Docker](https://en.wikipedia.org/wiki/Docker_(software)) and start using GOW!

## How does it work?

We bring together a few different components:

 - [Moonlight](https://moonlight-stream.org/): An open source implementation of NVIDIA's GameStream protocol. You can stream your collection of PC games from your GameStream-compatible PC to any supported device and play them remotely

 - [Sunshine](https://github.com/loki-47-6F-64/sunshine): An opensource Gamestream host for Moonlight. This gives us the ability to stream from a Linux box since it's not tied to the proprietary Nvidia GameStream (Windows only and not opensource)

 - [Docker](https://en.wikipedia.org/wiki/Docker_(software)): The platform that we use in order to deliver software packages (called containers) that you can easily run without having to manually install and configure everything

 - [Xorg](https://en.wikipedia.org/wiki/X.Org_Server): The window system that we use in order to manage and display graphical applications ([GUI](https://en.wikipedia.org/wiki/Graphical_user_interface))

 - [PulseAudio](https://en.wikipedia.org/wiki/PulseAudio): The software that will manage audio for our GUIs

 - [RetroArch](https://en.wikipedia.org/wiki/RetroArch): An open source, cross-platform frontend for emulators, game engines, and more!

<p align="center">
  <img width="300" src="{{ '/assets/img/gow-diagram.svg' | relative_url}}">
</p>

 Head over to the [components overview]({{ site.baseurl }}{% link _overview/components-overview.md %}) if you are interested in how these pieces of software are tied together by GOW

