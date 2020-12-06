
<div id="model-number" class="white-popup mfp-hide">

# Model Number

This address stores model number of DYNAMIXEL

</div>

<div id="model-information" class="white-popup mfp-hide">

# [Model Information](#model-information)

Represents product information.

</div>

<div id="firmware-version" class="white-popup mfp-hide">

# Firmware Version

This address stores firmware version of DYNAMIXEL.

</div>

<div id="id" class="white-popup mfp-hide">

# ID

{% include en/dxl/control_table_id.md passed_ref = page.tab_ref.ref1.product_group %}

</div>

<div id="baud-rate" class="white-popup mfp-hide">
{% include en/dxl/control_table_baudrate_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="return-delay-time" class="white-popup mfp-hide">
{% include en/dxl/control_table_return_delay_time.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="drive-mode" class="white-popup mfp-hide">
{% include en/dxl/control_table_drivemode.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="operating-mode" class="white-popup mfp-hide">
{% include en/dxl/control_table_mx_opmode_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="secondary-shadow-id" class="white-popup mfp-hide">
{% include en/dxl/control_table_shadowid.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="protocol-type" class="white-popup mfp-hide">
{% include en/dxl/control_table_protocolversion.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="homing-offset" class="white-popup mfp-hide">
{% include en/dxl/control_table_homingoffset.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="moving-threshold" class="white-popup mfp-hide">
{% include en/dxl/control_table_movingthreshold.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="temperature-limit" class="white-popup mfp-hide">
{% include en/dxl/control_table_temp_limit_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="max-voltage-limit" class="white-popup mfp-hide">

# Min/Max Voltage Limit(32, 34)

These values are maximum and minimum operating voltages.
When current input voltage acquired from [Present Input Voltage(144)](#present-input-voltage144) exceeds the range of Max Voltage Limit(32) and Min Voltage Limit(34), Voltage Range Error Bit(0x01) and [Hardware Error Bit(0x80)](#hardware-error-status70) in the Hardware Error Status(70) are set.
If Input Voltage Error Bit(0x10) is configured in the Shutdown(63), [Torque Enable(64)](#torque-enable64) is cleared to ‘0’ and Torque is disabled.
For more details, please refer to the [Shutdown(63)] section.

|    Unit    | Value Range | Description |
|:----------:|:-----------:|:-----------:|
| About 0.1V |  60 ~ 140   | 6.0 ~ 14.0V |

</div>

<div id="min-voltage-limit" class="white-popup mfp-hide">

# Min/Max Voltage Limit(32, 34)

These values are maximum and minimum operating voltages.
When current input voltage acquired from [Present Input Voltage(144)](#present-input-voltage144) exceeds the range of Max Voltage Limit(32) and Min Voltage Limit(34), Voltage Range Error Bit(0x01) and [Hardware Error Bit(0x80)](#hardware-error-status70) in the Hardware Error Status(70) are set.
If Input Voltage Error Bit(0x10) is configured in the Shutdown(63), [Torque Enable(64)](#torque-enable64) is cleared to ‘0’ and Torque is disabled.
For more details, please refer to the [Shutdown(63)] section.

|    Unit    | Value Range | Description |
|:----------:|:-----------:|:-----------:|
| About 0.1V |  60 ~ 140   | 6.0 ~ 14.0V |

</div>

<div id="pwm-limit" class="white-popup mfp-hide">
{% include en/dxl/control_table_pwm_limit.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="velocity-limit" class="white-popup mfp-hide">
{% include en/dxl/control_table_vellimit.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="max-position-limit" class="white-popup mfp-hide">

### Min/Max Position Limit(48, 52)

These values limit maximum and minimum target positions for Position Control Mode(Joint Mode) within the range of 1 rotation(0 ~ 4,095). Therefore, Goal Position(116) should be configured within the position limit range. These values are not used in Extended Position Control Mode.

|    Unit    |      Value Range      |
|:----------:|:---------------------:|
| 0.088&deg; | 0 ~ 4,095(1 rotation) |

**NOTE** : Max Position Limit(48) and Min Position Limit(52) are only used in Position Control Mode with a single turn.
{: .notice}

</div>

<div id="min-position-limit" class="white-popup mfp-hide">

### Min/Max Position Limit(48, 52)

These values limit maximum and minimum target positions for Position Control Mode(Joint Mode) within the range of 1 rotation(0 ~ 4,095). Therefore, Goal Position(116) should be configured within the position limit range. These values are not used in Extended Position Control Mode.

|    Unit    |      Value Range      |
|:----------:|:---------------------:|
| 0.088&deg; | 0 ~ 4,095(1 rotation) |

**NOTE** : Max Position Limit(48) and Min Position Limit(52) are only used in Position Control Mode with a single turn.
{: .notice}

</div>

<div id="shutdown" class="white-popup mfp-hide">
{% include en/dxl/control_table_shutdown.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="torque-enable" class="white-popup mfp-hide">
{% include en/dxl/control_table_torque_enable.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="profile-velocity" class="white-popup mfp-hide">
{% include en/dxl/control_table_profile_velocity.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-position(132)" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_position.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="led" class="white-popup mfp-hide">
{% include en/dxl/control_table_led.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="status-return-level" class="white-popup mfp-hide">
{% include en/dxl/control_table_status_return_lv.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="registered-instruction" class="white-popup mfp-hide">
{% include en/dxl/control_table_reg_instruction.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="hardware-error-status" class="white-popup mfp-hide">

# Hardware Error Status

The Hardware Error Statusindicates hardware error status.

{% include en/dxl/control_table_shutdown.md passed_ref = page.tab_ref.ref1.product_group %}

</div>

<div id="velocity-i-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_velocity_pi_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="velocity-p-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_velocity_pi_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="position-d-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_position_pid_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="position-i-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_position_pid_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="position-p-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_position_pid_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="feedforward-2nd-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_position_pid_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="feedforward-1st-gain" class="white-popup mfp-hide">
{% include en/dxl/control_table_position_pid_gain.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="bus-watchdog" class="white-popup mfp-hide">
{% include en/dxl/control_table_buswatchdog.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="goal-pwm" class="white-popup mfp-hide">
{% include en/dxl/control_table_goal_pwm.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="goal-velocity" class="white-popup mfp-hide">
{% include en/dxl/control_table_goal_velocity.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="profile-acceleration" class="white-popup mfp-hide">
{% include en/dxl/control_table_profile_acceleration.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="profile-velocity" class="white-popup mfp-hide">
{% include en/dxl/control_table_profile_velocity.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="goal-position" class="white-popup mfp-hide">
{% include en/dxl/control_table_goal_position_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="realtime-tick" class="white-popup mfp-hide">
{% include en/dxl/control_table_realtime_tick.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="moving" class="white-popup mfp-hide">
{% include en/dxl/control_table_moving_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="moving-status" class="white-popup mfp-hide">
{% include en/dxl/control_table_moving_status.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-pwm" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_pwm.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-load" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_load_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-velocity" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_velocity.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-position" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_position.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="velocity-trajectory" class="white-popup mfp-hide">
{% include en/dxl/control_table_velocity_trajectory.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="position-trajectory" class="white-popup mfp-hide">
{% include en/dxl/control_table_position_trajectory.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-input-voltage" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_volt_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="present-temperature" class="white-popup mfp-hide">
{% include en/dxl/control_table_present_temp_2.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="indirect-address" class="white-popup mfp-hide">
{% include en/dxl/control_table_indirect_data.md passed_ref = page.tab_ref.ref1.product_group %}
</div>

<div id="indirect-data" class="white-popup mfp-hide">
{% include en/dxl/control_table_indirect_data.md passed_ref = page.tab_ref.ref1.product_group %}
</div>
