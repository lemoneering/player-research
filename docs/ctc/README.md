# Capacitive Touch Pad Controller

This is the chip that will be handling the 24-bit matrix that makes up the gesture-pad. 24-bits because this ist he minimum number of capacitive planes that we can address to perform all of the gestures that we want to detect. This includes the 2 diagonal axes, horizontal axis, vertical, and rotational. This does *not* control the physical switches that are intended to lie below the touch pad.

It's actual function is intended to be a mixture between how navigation works on a Blackberry CT keyboard.

The touchpad is a design we're making ourselves, not a part that we are purchasing to use as is.

## Concept

![mockup of the touch-capacitive pad](./images/20260226_182856.jpg)

This image shows a mockup of what we will be doing for the touch-capacitive pad. Each green shape in the enclosed portion, except for the green circles in the corners and center, are each representing one plane. There are 16 primary planes for diagonal and directional and 8 additional in-betweens for a more responsive rotational. There are 24 planes total which is why we've chosen a 24-channel IC to drive the pads and read their inputs.

The buttons at the corners and center are only representative of where the pad would be in relation to them on the PCB, they will be directly controlled by the MCU not any other controller.
