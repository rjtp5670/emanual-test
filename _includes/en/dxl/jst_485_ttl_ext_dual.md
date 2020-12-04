

{% if page.ref=='xw540-t140' or page.ref=='xw540-t260' %}

|           Item           |                            RS-485                            |
|:------------------------:|:------------------------------------------------------------:|
|          Pinout          |         `1` GND<br>`2` VDD<br>`3` DATA+<br>`4` DATA-         |
|         Diagram          |        ![](/assets/images/dxl/jst_b4beha_diagram.png)        |
|         Housing          |   ![](/assets/images/dxl/JST_EHR-4.png)<br />[JST EHR-04]    |
|        PCB Header        | ![](/assets/images/dxl/JST_B4B-EH-A.png)<br />[JST B4B-EH-A] |
|      Crimp Terminal      |                     [JST SEH-001T-P0.6]                      |
| Wire Gauge for DYNAMIXEL |                            21 AWG                            |

> JST Connector

|              Item              |                                                  Product Image                                                   |                         Pin Diagram                          |
|:------------------------------:|:----------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------:|
|    Cable Connector (Female)    |    ![](/assets/images/dxl/x/xw/xw_cable_connector_female_sa610_s4b.png) <br /> [SA610/S4B]{: target="_blank"}    | ![](/assets/images/dxl/x/xw/xw540_cableconnector_female.png) |
| In-Line Cable Connector (Male) | ![](/assets/images/dxl/x/xw/xw_in_line_cable_connector_male_sa611_p4b.png) <br /> [SA611/P4B]{: target="_blank"} |  ![](/assets/images/dxl/x/xw/xw540_cableconnector_male.png)  |
|     Rear Nut Mount (Male)      |     ![](/assets/images/dxl/x/xw/xw_rear_nut_mount_male_sa612_p4b.png) <br /> [SA612/P4B]{: target="_blank"}      |  ![](/assets/images/dxl/x/xw/xw540_cableconnector_male.png)  |

> Dust and Waterproof Cable Connector

{% else %}

|           Item           |                             TTL                              |                            RS-485                            |                            External Port                            |                             Dual Joint                              |
|:------------------------:|:------------------------------------------------------------:|:------------------------------------------------------------:|:-------------------------------------------------------------------:|:-------------------------------------------------------------------:|
|          Pinout          |                `1` GND<br>`2` VDD<br>`3` DATA                |         `1` GND<br>`2` VDD<br>`3` DATA+<br>`4` DATA-         |    `1` GND<br>`2` VDD<br>`3` PORT 1<br>`4` PORT 2<br>`5` PORT 3     |                 `1` PWM1<br>`2` PWM2<br>`3` ENABLE                  |
|         Diagram          |        ![](/assets/images/dxl/jst_b3beha_diagram.png)        |        ![](/assets/images/dxl/jst_b4beha_diagram.png)        |          ![](/assets/images/dxl/molex_5304705_diagram.png)          |         ![](/assets/images/dxl/molex_588988000_diagram.png)         |
|         Housing          |   ![](/assets/images/dxl/JST_EHR-3.png)<br />[JST EHR-03]    |   ![](/assets/images/dxl/JST_EHR-4.png)<br />[JST EHR-04]    | ![](/assets/images/dxl/molex_510210500.png)<br />[MOLEX 51021-0500] | ![](/assets/images/dxl/molex_510210300.png)<br />[MOLEX 51021-0300] |
|        PCB Header        | ![](/assets/images/dxl/JST_B3B_EH-A.png)<br />[JST B3B-EH-A] | ![](/assets/images/dxl/JST_B4B-EH-A.png)<br />[JST B4B-EH-A] | ![](/assets/images/dxl/molex_530470510.png)<br />[MOLEX 53047-0510] | ![](/assets/images/dxl/molex_533980371.png)<br />[MOLEX 53398-0371] |
|      Crimp Terminal      |                     [JST SEH-001T-P0.6]                      |                     [JST SEH-001T-P0.6]                      |                         [MOLEX 50079-8100]                          |                         [MOLEX 50058-8000]                          |
| Wire Gauge for DYNAMIXEL |                            21 AWG                            |                            21 AWG                            |                               26 AWG                                |                               26 AWG                                |
{% endif %}


[SA610/S4B]: https://weipuconnector.com/pro_show_296.htm
[SA612/P4B]: https://weipuconnector.com/pro_show_299.htm
[SA611/P4B]: https://weipuconnector.com/pro_show_297.htm
[JST EHR-03]: http://www.jst-mfg.com/product/pdf/eng/eEH.pdf
[JST EHR-04]: http://www.jst-mfg.com/product/pdf/eng/eEH.pdf
[JST B3B-EH-A]: http://www.jst-mfg.com/product/pdf/eng/eEH.pdf
[JST B4B-EH-A]: http://www.jst-mfg.com/product/pdf/eng/eEH.pdf
[JST SEH-001T-P0.6]: http://www.jst-mfg.com/product/pdf/eng/eEH.pdf
[MOLEX 51021-0500]: http://www.molex.com/molex/products/datasheet.jsp?part=active/0510210500_CRIMP_HOUSINGS.xml
[MOLEX 53047-0510]: http://www.molex.com/molex/products/datasheet.jsp?part=active/0530470510_PCB_HEADERS.xml
[MOLEX 50079-8100]: http://www.molex.com/molex/products/datasheet.jsp?part=active/0500798100_CRIMP_TERMINALS.xml
[MOLEX 53398-0371]: https://uk.farnell.com/molex/53398-0371/header-smt-vertical-1-25mm-3way/dp/1125353
[MOLEX 51021-0300]: https://www.molex.com/molex/products/datasheet.jsp?part=active/0510210300_CRIMP_HOUSINGS.xml
[MOLEX 50058-8000]: https://www.molex.com/molex/products/datasheet.jsp?part=active/0500588000_CRIMP_TERMINALS.xml
