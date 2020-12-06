{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}

The Temperature Limit(31) limits operating temperature of the DYNAMIXEL.
When the [Present Temperature(146)](#present-temperature-{{ passed_model }}){: .popup2} is greater than the Temperature Limit(31), the **Over Heating Error Bit(0x04)** and **Hardware Error Bit(0x80)** in the [Hardware Error Status(70)](#hardware-error-status-{{ passed_model }}){: .popup2} will be set. If Overheating Error Bit(0x04) is configured in the [Shutdown(63)](#shutdown-{{ passed_model }}){: .popup2}, [Torque Enable(64)](#torque-enable-{{ passed_model }}){: .popup2} is cleared to ‘0’ and DYNAMIXEL's torque will be disabled.
See the Shutdown(63) for more detailed information.

|     Unit     | Value Range | Description  |
|:------------:|:-----------:|:------------:|
| About 1&deg; |   0 ~ 100   | 0 ~ 100&deg; |

**CAUTION** : Do not set this value higher than its default. In case that DYNAMIXEL encounters temperature warning alarm (Overheating Error Bit(0x04)), let it cool for 20 minutes or more. Otherwise, it may cause severe damage in operating.
{: .notice--warning}
