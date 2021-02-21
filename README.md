# The Settlers 4: Coalfix Plugin

![coalfix](coalfix.png)

By default, the size of your economy is limited by the so called coal bug. That is when a players economy consumes more goods than the game can assign jobs to carriers. Since coal is the  the most used good it is usually the first good being affected - ultimately leading to starvation at the smiths or smelters although more than enough coal is being produced. 

This plugin for The Settlers 4 fixes the coal bug. 

There is a [German translation for this README](README_DE.md). Please note that it may be outdated.


![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)



## Features

* Fixes the coal bug - for coal or any other good.
* Removes the delay when assigning a job to a carrier. Carriers will react much quicker to your commands.
* Compatibility: Works with the Gold Edition and the History Edition of The Settlers 4.
* Multiplayer interoperability: All participants **must** use the plugin - otherwise the game will desync.



## How to use

You need an ASI Loader to use this plugin. I recommend [The Settlers 4: ASI Loader](https://github.com/nyfrk/Settlers4-ASI-Loader) as it works nicely with the Gold and History Edition of The Settlers 4 and does not require any configuration. 

1. [Download](https://github.com/nyfrk/Settlers4-Coalfix/releases) a release.
2. Unpack the files into your `plugins` directory.
3. Start the game. The plugin will load automatically.

To uninstall the plugin remove `CoalFix.asi` from your `plugins` directory. 



## Known Problems

* This plugin does not really fix the coal bug but instead pushes the limit. Instead of assigning a job to a carrier every 16 ticks, we now assign a job every tick. To really fix the bug we would have to loop the open jobs and assign a carrier as long as there is a free carrier left.



## Issues and Questions

The project uses the Github Issue tracker. Please open a ticket [here](https://github.com/nyfrk/Settlers4-Coalfix/issues). 



## Contribute

The official repository of this project is available at https://github.com/nyfrk/Settlers4-Coalfix. 

#### Compile it yourself

Download Visual Studio 2017 or 2019 with the C++ toolchain. The project is configured to build it with the Windows XP compatible **v141_xp** toolchain. However, you should be able to change the toolchain to whatever you like. No additional libraries are required so it should compile out of the box.

#### How does this plugin work?

The game assigns jobs every 16 ticks (~1.14 s). When creating a job the game imposes a delay of 32 ticks (~2.28 s). The plugin decreases the timings to 1 tick (~0.07 s) for both occasions and thus pushes the limit that ultimately leads to the coal bug.

## License

The project is licensed under the [MIT](LICENSE.md) License. 
