# canhut
## Overview
`canhut` is a GUI-enriched CAN signal visualizer for FDC. It consists of the CAN-to-UDP routing program on FDC called `cannelloni`, an the same tool executed on ubuntu PC. They accomplish a CAN message mirroring from FDC's SocketCAN to ubuntu's SocketCAN. Most important, a CAN DBC and signal visualizer tool called `cabana` on ubuntu PC which can read frames from SocketCAN and plotting it on to the GUI according to the decode from loaded DBC file.

    ┌─────────┐  eth   ┌───────┐
    │ ubuntu  ├────────┤  FDC  ├────────────┐ ...... ───────┐
    └─────────┘        └──┬──┬─┘            │               │
                          │  └──────────┐   └───────┐       └───────┐
                          │ GBDC CAN    │ CAN1      │ CAN2          │ CAN_n
                      ┌───┴───┐     ┌───┴───┐   ┌───┴───┐       ┌───┴───┐    
                      │ BMS   │     │ ECUs  │   │ ECUs  │       │ ECUs  │
                      └───────┘     └───────┘   └───────┘       └───────┘
