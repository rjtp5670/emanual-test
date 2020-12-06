
<!-- ### <a data-tab-name="{{ page.tab_title2 | downcase }}" name="model-number"></a> -->

<div id="model-number-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Model Number

This address stores model number of DYNAMIXEL.

</div>

<div id="model-information-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Model Information

This address stores model number of DYNAMIXEL.

</div>

<div id="firmware-version-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Firmware Version

This address stores firmware version of DYNAMIXEL.

</div>

<div id="id-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# ID

{% include en/dxl/control_table_id.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="baud-rate-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Baudrate

{% include en/dxl/control_table_baudrate_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>


<div id="return-delay-time-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Return Delay Time

{% include en/dxl/control_table_return_delay_time.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="drive-mode-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Drive Mode

{% include en/dxl/control_table_drivemode.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="operating-mode-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Operating Mode

{% include en/dxl/control_table_mx_opmode_2.md passed_model = page.tab_ref.ref2.model passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="secondary-shadow-id-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Secondary(Shadow) ID

{% include en/dxl/control_table_shadowid.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="protocol-type13-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Protocol Type

{% include en/dxl/control_table_protocolversion.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="homing-offset-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Homing Offset

{% include en/dxl/control_table_homingoffset.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="moving-threshold-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Moving Threshold

{% include en/dxl/control_table_movingthreshold.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="temperature-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Temperature Limit

{% include en/dxl/control_table_temp_limit_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="max-voltage-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Min/Max Voltage Limit

These values are maximum and minimum operating voltages.
When current input voltage acquired from [Present Input Voltage(144)](#present-input-voltage-{{ passed_model }}){: .popup2} exceeds the range of Max Voltage Limit(32) and Min Voltage Limit(34), Voltage Range Error Bit(0x01) and [Hardware Error Bit(0x80)](#hardware-error-status-{{ passed_model }}){: .popup2} in the Hardware Error Status(70) are set.
If Input Voltage Error Bit(0x10) is configured in the Shutdown(63), [Torque Enable(64)](#torque-enable-{{ passed_model }}){: .popup2} is cleared to ‘0’ and Torque is disabled.
For more details, please refer to the [Shutdown(63)](#shutdown-{{ passed_model }}){: .popup2} section.

|     Unit      | Value Range |  Description   |
| :-----------: | :---------: | :------------: |
| About 0.1 [V] |  60 ~ 160   | 6.0 ~ 16.0 [V] |

</div>

<div id="min-voltage-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Min/Max Voltage Limit

These values are maximum and minimum operating voltages.
When current input voltage acquired from [Present Input Voltage(144)](#present-input-voltage-{{ passed_model }}){: .popup2} exceeds the range of Max Voltage Limit(32) and Min Voltage Limit(34), Voltage Range Error Bit(0x01) and [Hardware Error Bit(0x80)](#hardware-error-status-{{ passed_model }}){: .popup2} in the Hardware Error Status(70) are set.
If Input Voltage Error Bit(0x10) is configured in the Shutdown(63), [Torque Enable(64)](#torque-enable-{{ passed_model }}){: .popup2} is cleared to ‘0’ and Torque is disabled.
For more details, please refer to the [Shutdown(63)](#shutdown-{{ passed_model }}){: .popup2} section.

|     Unit      | Value Range |  Description   |
| :-----------: | :---------: | :------------: |
| About 0.1 [V] |  60 ~ 160   | 6.0 ~ 16.0 [V] |

</div>

<div id="pwm-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# PWM Limit

{% include en/dxl/control_table_pwm_limit.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="velocity-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Velocity Limit

{% include en/dxl/control_table_vellimit.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="max-position-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Max Position Limit

{% include en/dxl/control_table_positionlimit.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="min-position-limit-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Min Position Limit

{% include en/dxl/control_table_positionlimit.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="shutdown-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Shutdown

{% include en/dxl/control_table_shutdown.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="torque-enable-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Torque Enable

{% include en/dxl/control_table_torque_enable.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="led-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_led.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="status-return-level-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_status_return_lv.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>


<div id="registered-instruction-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_reg_instruction.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="hardware-error-status-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

The Hardware Error Status(70) indicates hardware error status.
{% include en/dxl/control_table_shutdown.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="velocity-i-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_velocity_pi_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="velocity-p-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_velocity_pi_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="position-d-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}
</div>


<div id="position-i-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="position-p-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="feedforward-1st-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="feedforward-2nd-gain-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="position-pid-gain80-82-84-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="feedforward-1st2nd-gains88-90-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_pid_gain.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="bus-watchdog-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_buswatchdog.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="goal-pwm-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_goal_pwm.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="goal-velocity-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_goal_velocity.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="profile-acceleration-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Profile Acceleration

{% include en/dxl/control_table_profile_acceleration.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="profile-velocity-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

# Profile Velocity

{% include en/dxl/control_table_profile_velocity.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="goal-position-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_goal_position_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>


<div id="realtime-tick-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_realtime_tick.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="moving-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_moving_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="moving-status-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_moving_status.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="present-pwm-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

This value indicates present PWM. For more details, please refer to the [Goal PWM(100)](#goal-pwm-{{ passed_model }}){: .popup2}.

</div>

<div id="present-load-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_present_load_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="present-velocity-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

This value indicates present Velocity. For more details, please refer to the [Goal Velocity(104)](#goal-velocity-{{ passed_model }}){: .popup2}.

</div>

<div id="present-position-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_present_position.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="velocity-trajectory-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

This is a target velocity trajectory created by Profile. Operating method can be changed based on control mode. For more details, please refer to the [Profile Velocity(112)](#profile-velocity-{{ passed_model }}){: .popup2}.

1. **Velocity Control Mode** : When Profile reaches to the endpoint, Velocity Trajectory(136) becomes equal to [Goal Velocity(104)](#goal-velocity-{{ passed_model }}){: .popup2}.
2. **Position Control Mode, Extended Position Control Mode** : Velocity Trajectory is used to create [Position Trajectory(140)](#position-trajectory-{{ passed_model }}){: .popup2}. When Profile reaches to an endpoint, Velocity Trajectory(136) is cleared to '0'.

</div>

<div id="position-trajectory-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_position_trajectory.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="present-input-voltage-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_present_volt_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="present-temperature-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_present_temp_2.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="indirect-address-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_indirect_data.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>

<div id="indirect-data-{{ page.tab_ref.ref2.model }}" class="white-popup mfp-hide">

{% include en/dxl/control_table_indirect_data.md passing_model = page.tab_ref.ref2.model passed_ref = page.tab_ref.ref2.product_group %}

</div>
