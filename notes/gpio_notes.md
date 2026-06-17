# GPIO
- general purpose input output
- programmable pins for input (recieve data) and output (send data)
- can have additional options
  - analog
  - alternate function (AF) --> for communcation protocols
  - open drain/collector
## General workflow for configuring a pin
- select pin function
- if gpio, select direction
- enable pull up/down resistor
  -  give the pin a known default state
      - pull up --> default state == HIGH
      - pull down --> default state == LOW
  - without, pin can pick up noise  
- if output, select output type and output speed
