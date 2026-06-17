# Universal Asynchronous Reciever Transmitter
- serial: sends data one bit at a time
- full duplex: can go both ways simultaneously
- Transmitter (Tx) sends to reciever (Rx)
- asynchronous: no clock so both devices need to agree on baud rate, data bits, parity bits, and stop bits
    - baud rate determines when to sample the data
    - check reference manual for eq (stm32)
        - baud = f_ck /(8 * (2 - over8) * USARTDIV)
- its really only meant for two devices so it doesn't allow for multiple devices on the same bus
- idle is normally always high, so when the line goes low, thats how the reciever knows the message is starting, then it goes back to idle when done
