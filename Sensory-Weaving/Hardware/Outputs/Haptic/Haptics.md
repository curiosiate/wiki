---
title: Haptic Outputs
description: haptics vibrate, buzz, zap, push, poke prod and more. Anything to do with touch, tactile perception modulation, will be in this area. 
layout: post
nav_order: 1
has_children: true
parent: Outputs
grand_parent: Hardware
---

# Overview
There are various types of haptic output devices, the most common for wearables at least in terms of price will be vibration based feedback. 

There may be need to determine the correct output based on need of feedback and relevant [Neurospec](https://wiki.curiosiate.com/Sensory-Weaving/Neurospec/Neurospec.md)


# Vibration
Haptics using vibration can modulate and encode information over 3 main modalities of discernment, based on different sensors and perceptual biases - these are rough guidelines, but not hard and fast because the mind and perception is pliable.

## ERMs 
Or, eccentric rotating mass - these haptics have slower spin up time, and less control over frequency and shaping of feedback to the end user. 
**Pros**
Cheap, easy to power and drive with basic DC signal at different voltage levels. 
**Cons**
Slow response time



## LRAs
these are more complex to drive, signal wise. They allow greater control by using A/C to drive, and this allows inverting the signal to bring the moving mass to a stop with much higher response and precision. (known as braking)

**Pros**
wideband frequency response - can provide many more points of articulation within the sensory thread crafted
braking - ability to slice up signals at even higher rates, like having a high refresh rate monitor


**Cons**
requires an A/C signal to fully take advantage while driving. 
Needs custom drivers/circuit to run, which can be larger footprint if not going custom PCB.
Cost - they can be costly, but can also be found second hand for cell phone repair motors. 

## VoiceCoils
More similar to the transducers found in speakers, they will still drive similar to LRAs, except in this case instead of the LRAs, the magnetic mass is what moves here instead. 
Otherwise largely similar to LRAs, perhaps requiring more power at some points.

## Piezoelectrics
A low power, high voltage driver - able to be driven from chips such as the DRV8662

# Temperature
Temperature may seem like a useful information channel, and it can be, contextually, depending on the information one wishes to convey over it. Tactile response is slower, and has interesting mix-in effects with vibratory which leads to tactile illusions moving the sensation of thermal over the vibration location's perceived point of contact. 
When used correctly, this is a helpful feature, but if attempting to mix in thermals for feedback it also is important to consider when designing that feedback. 

**Pros**
can take advantage of thermal tactile illusions

**Cons**
those same illusions
"refresh rate"

# Electrotactile
A much more interesting utility, however also perhaps one of the more tricky to do safely, and DIY manner for now. From titanium microneedles to driving voltages to overcome resistance barriers at lower voltages by using high frequencies, timing and power is everything. Misjudge that, and you can cause more than just sensation, you can introduce pain, cell damage.  The conductivity also fluctuates, meaning one must be within safe limits there accomodating that variable into the driver and safety mechanisms.

**Pros**
high spatial density

**Cons**
complex driving, if doing it safely.
