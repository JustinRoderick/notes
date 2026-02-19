Just-In-Time Compilation is when code gets compiled into machine code while a program is running, rather than before.

## Difference Between [[Ahead-Of-Time Compilation|Regular Compilation]]

JIT
- Compiles code while the program runs
- Has to be very fast
- Can use the runtime info the make smarter optimizations
- More overhead

Regular Compilation
- Compiles everything before the program runs
- Takes their time with optimizations
- Produces an executable binary which is ran after compilation
- No runtime overhead

## When Not To Use JIT

- When predictability matters; JITs have a warm up period where performance might be unpredictable
- Requires more resources (RAM, CPU cycles)
- Embedded systems, IoT devices, and other resource constrained envs can not always afford the overhead of the needed resources
- Security, no runtime surprises.
