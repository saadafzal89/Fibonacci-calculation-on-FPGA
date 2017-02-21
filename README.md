# Fibonacci-calculation-on-FPGA
Fibonacci calculator running as a custom peripheral to the ARM processor on the ZedBoard

To enable communication with this
peripheral, implemented a custom memory map that associates different
FPGA resources with a specific address. Although the AXI interface could provide this
same functionality, in this project a specialized abstract interface was used (i.e., a virtual
board) with a memory-map interface that is built on top of the AXI interface. This virtual
board enables us to potentially use the exact same code on different boards, instead of
porting the memory-map code for different board interfaces.
