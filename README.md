# Ensemble
A CAN bus based framework for connecting devices and orchestrating interactions between devices.

## About
This project seeks to define a standard and a reference implementation to allow connecting devices and defining interactions (application layer) to allow inputs to be gathered and outputs to be triggered. The standard will support on bus publishing of device specifications to allow for new devices to be placed on network without needing to re-compile code (dynamic discovery and hot-swappability).

Examples of where this standard could be used:
* museum interactivity with multiple stages which need to be tracked -- CAN bus supports long connection lengths
* interactive art pices -- large numbers of inputs (buttons, sensors, etc) and outputs (audio players, LEDs, displays, motors, etc) can be connected together and interactivity designed

### Why CAN bus? (TODO)

## Specification (TODO)
* universal clock -- channel dedicated to clock syncing and a standard for collective sync -- allowing for synchonizing time based events (possibly with triggers being sent with timestamps or at least epoch counts based on current time)
* nodes are responsible for pre-processing data -- for example, if a device supports user input through buttons -- the device is responsible for debouncing and only transmitting triggers
* auto-discovery -- when a device is added to a network it broadcasts its identity on a reserved channel to allowe control board to provide information about which channel space is free (if device is not yet configured)
* application design -- the control node will provide lots of stuff but also should provide a runtime (unknow yuet what type) to allow for manipulation of data through scripts. it will also allow -- in a basic way -- to declaratively route signals

### channels and hierachy
