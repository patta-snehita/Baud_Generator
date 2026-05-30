Baud Generator (Verilog)
A parameterized Baud Rate Generator designed for UART communication systems.

Features
* Configurable clock frequency and baud rate using parameters
* Generates a single-cycle `baud_tick` pulse
* Supports different UART baud rates without modifying RTL code
* Synchronous counter-based implementation

Parameters
* `clock_freq` : System clock frequency
* `baud_rate` : Desired UART baud rate

Working Principle
The baud generator divides the system clock according to:
baud_count = clock_freq / baud_rate
When the internal counter reaches `baud_count - 1`, a `baud_tick` pulse is generated and the counter resets.

Example
For:
* Clock Frequency = 100 MHz
* Baud Rate = 9600

The generated `baud_tick` is used by UART TX/RX modules to control bit transmission and reception timing.
