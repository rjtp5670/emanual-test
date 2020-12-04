## [Communication Circuit](#communication-circuit)
To control the DYNAMIXEL actuators, the main controller needs to convert its UART signals to the half duplex type. The recommended circuit diagram for this is shown below.

{% if page.product_group=='dxl_ax' %}
### [TTL Communication](#ttl-communication)
![](/assets/images/dxl/ttl_circuit.png)

{% else %}

### [TTL Communication](#ttl-communication)
![](/assets/images/dxl/ttl_circuit.png)

### [RS-485 Communication](#rs-485-communication)
![](/assets/images/dxl/485_circuit.png)

The power of DYNAMIXEL is supplied via Pin1(-), Pin2(+).  
(The above circuit is built into DYNAMIXEL's controller only)  
In the above circuit diagram, the direction of data signal of TxD and RxD in the TTL Level is determined according to the level of DIRECTION 485 as follows:  
In case of DIRECTION485 Level = High: The signal of TxD is output to D+ and D-  
In case of DIRECTION485 Level = Low: The signal of D+ and D- is output to RxD  

{% endif %}
