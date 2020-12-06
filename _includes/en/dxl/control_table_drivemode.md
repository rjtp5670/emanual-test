{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

# Drive Mode

{% if passed_product_group=='dxl_x430' %}This address configures Drive Mode of DYNAMIXEL. Drive Mode is available from the **firmware V38**.
{% else %}The Drive Mode(10) configures Drive Mode of DYNAMIXEL.
{% endif %}


|     Bit     |                Item                 | Description                                                                                                                                                                                                                                                                                                                                      |
|:-----------:|:-----------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 7(0x80) |                  -                  | Unused, always ‘0’                                                                                                                                                                                                                                                                                                                               |
| Bit 6(0x40) |                  -                  | Unused, always ‘0’                                                                                                                                                                                                                                                                                                                               |
| Bit 5(0x20) |                  -                  | Unused, always ‘0’                                                                                                                                                                                                                                                                                                                               |
| Bit 4(0x10) |                  -                  | Unused, always ‘0’                                                                                                                                                                                                                                                                                                                               |
| Bit 3(0x08) |                  -                  | Unused, always ‘0’                                                                                                                                                                                         |{% if passed_product_group== 'xl330' or 'dxl_x430' or passed_product_group=='dxl_x540' or passed_product_group=='dxl_xw540'or passed_product_group=='dxl_xl430' or passed_product_group=='dxl_mx2' %}
| Bit 2(0x04) |        Profile Configuration        | **[0]** Velocity-based Profile:  Create a Profile based on Velocity<br />**[1]** Time-based Profile: Create Profile based on time <br />※ See [What is the Profile](#what-is-the-profile) |{% else %}
| Bit 2(0x04) |                  -                  | Unused, always ‘0’                                                                                                                                                                                          |{% endif %}{% if passed_product_group=='dxl_x540' or passed_product_group=='dxl_ex' or passed_model=='mx-106-2' or passed_model=='mx-106' %}
| Bit 1(0x02) | Master/Slave Mode<br />(Dual Joint) | **[0]** Master Mode: Operate as a Master DYNAMIXEL.<br />**[1]** Slave Mode: Operate as Slave DYNAMIXEL                                                                                                          |{% else %}
| Bit 1(0x02) |                  -                  | Unused, always ‘0’                                                                                                                                                                                           |{% endif %}
| Bit 0(0x01) |         Normal/Reverse Mode         | **[0]** Normal Mode: CCW(Positive), CW(Negative)<br />**[1]** Reverse Mode: CCW(Negative), CW(Positive)                                                                                                  |

{% if passed_product_group=='dxl_mx2' or passed_product_group=='dxl_x540' or passed_product_group=='dxl_xw540' or passed_product_group=='dxl_x430' or passed_product_group=='dxl_xl430' %}
**NOTE** : Time-based Profile is available from **firmware V42**.
{: .notice}
{% else %}{% endif %}

{% capture notice_01 %}
**NOTE** : If the value of Bit 0(Normal/Reverse Mode) of the Drive Mode(10) is set to `1`, rotational direction is inverted.
Thus, {% if passed_product_group=='dxl_mx2' or passed_product_group=='dxl_x540'  or passed_product_group=='dxl_xw540' %}**Position**, **Velocity**, **Current**, **PWM**{% else %}**Goal Position**, **Present Position**{% endif %} will have a inverted direction.
This feature can be very useful when configuring symmetrical joint or wheel system.
{% endcapture %}
<div class="notice">{{ notice_01 | markdownify }}</div>

{% if passed_model=='mx-106' or passed_product_group=='dxl_ex' %}
{% capture drivemode %}
**CAUTION** : When MX-106 and EX-106+ are set to Wheel Mode(endless), Normal/Reverse Mode is not available.
Normal/Reverse Mode is activated under Joint Mode and Multi-turn Mode.
Please refer to [CW/CCW Angle Limit](#cwccw-angle-limit6-8) for configuring Operation Type.
{% endcapture %}
<div class="notice--warning">{{ drivemode | markdownify }}</div>
{% else %}{% endif %}

{% if passed_product_group=='dxl_x540' or passed_product_group=='dxl_ex' or passed_model=='mx-106-2' or passed_model=='mx-106' %}
#### Dual Mode
Dual Mode is intended to combine two DYNAMIXEL into a single joint to enhance the performance.
In order to use Dual Mode, Slave DYNAMIXEL should be connected to Master DYNAMIXEL with the Sync Cable.

Please note that the Slave DYNAMIXEL is directly controlled only by the PWM signal from the Master DYNAMIXEL through the Sync Cable.
Thus, {% if passed_product_group=='dxl_ex' or passed_model=='mx-106' %}Goal Position, Moving Speed{% else %}Goal Position, Goal Velocity, Goal Current, Goal PWM{% endif %} of the Slave DYNAMIXEL are unused and ignored.

The rotational direction of Slave DYNAMIXEL is decided by **the type of Sync Cable** rather than the Normal/Reverse Mode setting of Slave DYNAMIXEL.
The twisted sync cable will actuate the Slave DYNAMIXEL to the opposite direction of the Master DYNAMIXEL while regular sync cable actuate to the same direction.
{: .notice}

{% if passed_product_group=='dxl_x540' %}
![](/assets/images/dxl/x/x-series_dual_joint.png)
{% else %}
![](/assets/images/dxl/ex/ex-106_dual.png)
{% endif %}

|     Sync Cable     | Description                                                                                                                                               |
|:------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Regular Sync Cable | Slave DYNAMIXEL is controlled by the `PWM Signal` from the Master DYNAMIXEL.<br>Master and Slave DYNAMIXEL rotate in the **same direction**.              |
| Twisted Sync Cable | Slave DYNAMIXEL is controlled by the `Inverted PWM Signal` from the Master DYNAMIXEL.<br>Master and Slave DYNAMIXEL rotate in the **opposite direction**. |

{% capture dual_frame %}
**CAUTION** : If Master and Slave are not physically connected by frame, both DYNAMIXEL may not perfectly synchronized due to the load applied on each DYNAMIXEL.
Please use appropriate frame to connect DYNAMIXEL in Dual Mode.
{% if passed_product_group=='dxl_x540' %}
![](/assets/images/dxl/x/x-series_dual_joint_frame.png)
{% else %}
![](/assets/images/dxl/ex/ex-106+_fr08-h110_fr08-d101.png)
{% endif %}
{% endcapture %}
<div class="notice--warning">{{ dual_frame | markdownify }}</div>

{% else %}{% endif %}
