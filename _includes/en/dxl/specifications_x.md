{% assign item_data = site.data.dxl_x_info[include.passed_ref] %}

<!-- item_data is the data to check the selected product in the tab  -->

| Item                          | Specifications                                              |
| :---------------------------- | :---------------------------------------------------------- |
| MCU                           | {{ item_data.mcu }}                |
| Position Sensor               | {{ item_data.encoder }}            |
| Motor                         | {{ item_data].motor }}             |
| Baud Rate                     | {{ item_data.baudrate }}           |
| Control Algorithm             | {{ item_data.control }}            |
| Resolution                    | {{ item_data.resolution }}         | {% if item_data.backlash != 'N/A' %}
| Backlash                      | {{ item_data.backlash }}           | {% else %}{% endif %}
| Operating Modes               | {{ item_data.mode_en }}            |
| Weight                        | {{ item_data.weight }}             |
| Dimensions (W x H x D)        | {{ item_data.dimensions }}         |
| Gear Ratio                    | {{ item_data.gearratio }}          |
| Stall Torque                  | {{ item_data.stalltorque }}        |
| No Load Speed                 | {{ item_data.noloadspeed }}        | {% if item_data.radialload_en != 'N/A' %}
| [Radial Load]{: .popup}       | {{ item_data.radialload_en }}      | {% else %}{% endif %}{% if item_data.axialload != 'N/A' %}
| [Axial Load]{: .popup}        | {{ item_data.axialload }}          | {% else %}{% endif %}
| Operating Temperature         | {{ item_data.temperature }}        | {% if page.product_group=='dxl_xw540' %}
| **Ingress Protection rating** | **IP 68 (1 m, 24 hr)**             | {% else %}{% endif %}
| Input Voltage                 | {{ item_data.voltage_en }}         |
| Command Signal                | {{ item_data.command }}            |
| Protocol Type                 | {{ item_data.protocoltype }}       |
| Physical Connection           | {{ item_data.physicalconnection }} |
| ID                            | {{ item_data.id }}                 |
| Feedback                      | {{ item_data.feedback }}           |
| Part Material                 | {{ item_data.material }}           |
| Standby Current               | {{ item_data.standbycurrent }}     |

[radial load]: /assets/images/dxl/axial_radial_load.png
[axial load]: /assets/images/dxl/axial_radial_load.png
