# Inter-Intergrated Circuit
- consists of Master and Slaves
- serial and synchronous
- half-duplex: goes one way at a time (either sends or recieves)
- uses two wires:
  - SDA (data): sends and recieves
  - SCL (serial clock): carries clock signal
- data is sent in messages:
    - each messages has a start condition, address frame, read/write, Ack/Nack, data frame, Ack/Nack, stop condition
        - start: SDA goes HIGH --> LOW before SCL does
        - stop: SDA goes LOW --> HIGH before SCL does
        - address frame (usually 7 but up to 10 bits): selects the device to recieve the data
        - read/write (1 bit): signals whether the devices is sending or recieving
        - Ack/Nack (1 bit): signals if the device has succesfully acknowledged
        - data frame (8 bits): the data being sent or recieved
    - if the receiver has more than one register, you must specify the register address before the data
## Pros
- only 2 pins
- built in addressing/acknowledgment
- mutliple master support
- standardized protocol
## Cons
- slower
- can have address conflicts
- complex messaging protocol (more software)
