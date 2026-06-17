# Serial Peripheral Interface
- master and slave configuration
- synchronous: shares a clock (provided by master)
- serial and full duplex
- has four signals:
    - Sclk: serial clock
    - MOSI: Master out, Slave In (master sending data)
    - MISO: Master In, Slave Out (master recieving data)
    - SS: slave select
        - active low
        - Each slave can have its own select wire or we can daisy chain
            - daisy chaining: one SS line shared among all the slaves, but the masters output goes to the first slaves input, the first slaves output goes to the second slaves input. This process keeps going until the last slave, whose output goes to the master input.
## Pros
- Fast
- no complex messaging protocol
- can talk to many devices
## Cons
- uses A LOT of pins
- no standard protocol (some send MSB first and others LSB)
- no multi-master support
