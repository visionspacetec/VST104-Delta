# VST104 Board Delta - double MCU OBC for PC104
This repository contains the KiCad project and other documents created during the development of Board Delta under [VST104 project](https://github.com/visionspacetec/VST104/). This PC104 CubeSats module is a double redundant onboard computer accomodating all of the features of the [Board Siera](https://github.com/visionspacetec/VST104-Sierra) together with dual redundancy.

<p align="center">
  <br>
  <img src=/gallery/3Dexport/top.png width=49%/>
  <img src=/gallery/3Dexport/bottom.png width=49%/>
  <br><br>
  <b>Fig 1.</b> Board Delta OBC module 3D visualisation top (left) and bottom (right) side.
  <br><br>
</p>


## Specifications
This double onboard computer PC104 module implements [Board Sierra](https://github.com/visionspacetec/VST104-Sierra) in full dual redundancy. The original Sierra module was extended with its own mirrored copy resulting in two independent OBCs. Both of them share almost the same layout. Only small changes in tracing around the main header and flip of debug & program connector were required. Thanks to this approach, no software changes of the two OBCs are necessary, and both OBCs share very similar electrical characteristics. There is no tracing placed in the middle-top part of the board, just under the "VST104 Delta" marking. This provides enough space for the implementation of killing/switching logic between the OBCs.

**For more specifications wisit [Board Sierra repository](https://github.com/visionspacetec/VST104-Sierra).**

<p align="center">
  <br>
  <img src=/gallery/present/header_pinout.png width=60%/>
  <br><br>
  <b>Fig 2.</b> PC104 header pinout supported by this OBC module.
  <br><br>
</p>

## Debug & Program connector
Two separate 2x4 female format connectors on both boards sides are used for debugging and programming. SWI and UART5 interfaces of the boarded STM32 microprocessor are wired to this connector, as shown in figure 4. This interface is fully compatible with STM ST-Link family programmers. 

<p align="center">
  <br>
  <img src=/documents/deb_prog_pinout.png width=100%/>
  <br><br>
  <b>Fig 3.</b> Pinout of the debug and program connector for both OBCs.
  <br><br>
</p>
