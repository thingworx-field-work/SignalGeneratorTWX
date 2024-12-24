## Thingworx Signal generator

### Why use it?

In many apps you have to generate data that does not look completely random. This project helps you generate that data.

### How to use it?

* If you want to generate a chart, then use the `getNoise` service  `SignalGenerator` thing. This service returns a infotable with your data. This are the required parameters:
    * `scale`: how "contiguous" you want the signal to be
    * `amplitude`: how big is the dynamic part of the signal
    * `additiveGradient`: Gain, or by how much you want each point to grow
    * `offset`: offset the signal from 0 (smallest data point)
    * `intervalStart` and `intervalEnd`: the generated signal will sit between this two dates
    * `sampleTime`: in ms, how often should the signal change
* If you want to update a property value based, using a timer, you can create a thing that inherits  `SignalGeneratorTemplate`, and call `getNextValue`. The same parameters as above apply.

### Demo

Take a look at `SignalGeneratorDemo`.

![demo](https://i.imgur.com/WF8zlT9.png)

### How it works

It uses a [Perlin Noise 1D](https://en.wikipedia.org/wiki/Perlin_noise) generator.

# Disclaimer
By downloading this software, the user acknowledges that it is unsupported, not reviewed for security purposes, and that the user assumes all risk for running it.

Users accept all risk whatsoever regarding the security of the code they download.

This software is not an official PTC product and is not officially supported by PTC.

PTC is not responsible for any maintenance for this software.

PTC will not accept technical support cases logged related to this Software.

This source code is offered freely and AS IS without any warranty.

The author of this code cannot be held accountable for the well-functioning of it.

The author shared the code that worked at a specific moment in time using specific versions of PTC products at that time, without the intention to make the code compliant with past, current or future versions of those PTC products.

The author has not committed to maintain this code and he may not be bound to maintain or fix it.


# License
I accept the MIT License (https://opensource.org/licenses/MIT) and agree that any software downloaded/utilized will be in compliance with that Agreement. However, despite anything to the contrary in the License Agreement, I agree as follows:

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.

