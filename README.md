## APB_PROTOCOL
The APB protocol (Advanced Peripheral Bus) is a part of the AMBA (Advanced Microcontroller Bus Architecture) family developed by ARM. It is designed for simple, low-power peripheral communication and provides a low-bandwidth, low-latency connection between peripherals and the system bus. APB is often used in conjunction with higher-performance buses such as AHB (Advanced High-Performance Bus) or AXI (Advanced eXtensible Interface) for communicating with low-speed peripherals like timers, UARTs, or GPIOs.

#### APB Features:
Low complexity: Simple design for connecting low-speed peripherals.
Low power: Power-efficient due to its simplicity.
Single clock domain: APB operates synchronously with the system clock, simplifying its design.
Non-pipelined: Unlike AHB or AXI, APB does not support pipelining, which simplifies communication but sacrifices performance.

#### APB Transfer Phases:
IDLE: No data transfer is happening.
SETUP: The address and control signals are set up during this phase.
ACCESS: Data is transferred between the master and the slave.

#### APB Signals:
##### 1. PADDR (Peripheral Address)
Direction: From master to slave.
Description: This signal contains the address of the peripheral or register being accessed.

##### 2. PWRITE (Write Enable)
Direction: From master to slave.
Description: Determines the direction of data transfer. If PWRITE = 1, it indicates a write operation, and if PWRITE = 0, it indicates a read operation.

##### 3. PWDATA (Write Data)
Direction: From master to slave.
Description: The data to be written to the addressed peripheral during a write transaction.

##### 4. PRDATA (Read Data)
Direction: From slave to master.
Description: The data read from the addressed peripheral during a read transaction.

##### 5. PSEL (Peripheral Select)
Direction: From master to slave.
Description: This signal selects a particular slave device for communication. Only one peripheral can be selected at a time.

##### 6. PENABLE (Enable Signal)
Direction: From master to slave.
Description: Indicates the start of the data transfer in the access phase. The master asserts PENABLE high during the access phase to enable communication.

##### 7. PREADY (Peripheral Ready)
Direction: From slave to master.
Description: Indicates that the slave is ready to complete the data transfer. If PREADY is high, the data transfer completes in that cycle.

##### 8. PSLVERR (Slave Error)
Direction: From slave to master.
Description: This signal indicates an error condition on the APB bus. If asserted high, it indicates an error during the data transfer.

##### 9. PCLK (Peripheral Clock)
Direction: From system clock to peripherals.
Description: The clock signal for driving the APB logic.

##### 10. PRESETn (Peripheral Reset)
Direction: System to APB master and peripherals.
Description: An active-low reset signal that resets the state of the bus and peripherals.


![maxresdefault](https://github.com/user-attachments/assets/b218e323-1e3c-4280-b3a9-92eb73db6e82)

![dar1523383162089](https://github.com/user-attachments/assets/ef9b8ec5-129d-473f-8bba-102369071d2e)

![aps](https://github.com/user-attachments/assets/329600d7-f103-489d-9a06-de0344084b40)
