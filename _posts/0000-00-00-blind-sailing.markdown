---
layout: post
title: "Blind Sailing"
img: bs_overview.jpg # Add image post (optional)
date: 2016-7-10 12:55:00 +0300
description: Worked on the Olin Adaptive Sailing Team to create a system that enables blind sailors to compete in match races autonomously.
tag: [research, python, integration, user-oriented design]
---

I spent the summer between my first and second year of college working on the Olin Adaptive Sailing Team. Our goal was to create a system that enables blind sailors to compete in match races without a sighted guide and without the many pain points of the current system, the Homerus system.

### OUR PROBLEM

The Homerus system is over 20 years old, illegal in the US (the tilt sensor has mercury in it and the frequency of the radio that turns the sirens on and off is off-limits), difficult to learn, prohibitively expensive (over $4000), bulky, hard to setup, and annoying. It’s completely audio-based — match races involve two boats racing around a course of three buoys, and in the Homerus system, all of the buoys and boats are equipped with sirens that produce sounds of up to 113 decibels; to put that into perspective, a vacuum cleaner is normally about 70 decibels, a chainsaw is roughly 110, and a nearby thunderclap can be 120. All of which is to say, it can be extraordinarily difficult to hear the sound of the other boat’s siren or the buoys’ sirens over the sound of your own siren, located just a few feet away. The Homerus system was once truly revolutionary, and it has provided blind sailors the opportunity to sail independently, but it’s time for something new.

### OUR MISSION

That’s where we came in. We decided to focus our efforts this summer on replacing the sirens on the boats. The boat-sirens are important not only for broadcasting the boats’ positions, but also their tacks (which is determined by what side of the boat the bottom of the sail is on). Tack determines right of way and plays a big part in the strategy behind match racing. The Homerus system uses a tilt sensor and two different sirens to communicate both position and tack by making one of two sounds (using one of two sirens), depending on the tack.

### OUR PROTOTYPE

The prototype we produced after eight weeks of hard work is relatively simple and not eardrum-shattering.

Each boat has the same setup. We use a GPS sensor to collect location data and a potentiometer to measure the tack, as you can see in the picture on the left. The green part of the tack sensor attaches to the mast of the boat, and a similar but not-shown white piece clips on to the boom.

![tack](mary-keenan.github.io/assets/img/bs_tack.png "Tack")

This information is broadcasted by a Raspberry Pi via an ad-hoc network; the two Pis receive the data from both boats, process it, and communicate it to the blind sailors using text-to-speech. A diagram of our system is on the right!

![system diagram](mary-keenan.github.io/assets/img/bs_diagram.png "System Diagram")

Our program is very customizable; everything from how often the information is shared, what information is shared, the units for the information, and so on, can be adjusted. The blind sailors can receive regular updates as well as query the information whenever they want using a keypad (diagram on the left!). The information available includes the distance and relative direction from one boat to another, the tack of the other boat, and the distance and relative directions to each of the buoys (the coordinates of the buoys can be plugged in).

![tack](mary-keenan.github.io/assets/img/bs_keypad.png "Keypad")

The videos below shows two of our test sessions. We regularly tested our prototypes on our own and with blind sailors, and we incorporated their suggestions. The project isn’t done, but we made good progress, and we have some very happy sailors!

