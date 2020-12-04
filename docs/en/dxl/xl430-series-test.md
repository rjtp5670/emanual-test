---
layout: archive
lang: en
ref: xl430-w250
tab_ref:
  ref1:
    model: xl430-w250
    product_group: dxl_xl430
  ref2:
    model: xc430-w150
    product_group: dxl_x430
  ref3:
    model: xh430-w210
    product_group: dxl_x430
read_time: true
share: true
author_profile: false
permalink: /docs/en/dxl/x/x430-series/test
tabs: "DYNAMIXEL"
tab_title1: XL430-W250
tab_title2: XC430-W150
tab_title3: XH430-W210
sidebar:
title: XL430-W250-T
nav: "xl430-w250-test"
product_group: dxl_xl430
---

{::options parse_block_html="true" /}

<!-- 

{% capture Goal_Position %}

<div class="popup2" onclick="myFunction()">Goal Position
<div class="popuptext" id="myPopup"> {% include en/dxl/control_table_goal_position_2.md passed_ref = page.tab_ref.ref3.product_group %}</div>
</div>
{% endcapture %} 
-->

<!-- 테스트  시작 -->

<div id="test-popup" class="white-popup mfp-hide">
  {% include en/dxl/control_table_goal_position_2.md passed_ref = page.tab_ref.ref3.product_group %}
</div>

<div id="protocol-type" class="white-popup mfp-hide">
  {% include en/dxl/control_table_protocolversion.md passed_ref = page.tab_ref.ref3.product_group %}
</div>


[Show inline popup](#test-popup){: .popup2}

[Protocol Type](#protocol-type){: .popup2}


<!-- Or like so: -->


<!-- 

{% assign goal_pos = Goal_Position %}

{{ goal_pos }}

{% capture Temp_Table %}
| Address | Size<br>(Byte) | Data Name      | Access | Default<br />Value | Range | Unit |
|:-------:|:--------------:|:---------------|:------:|:------------------:|:-----:|:----:|
|    0    |       2        | {{ goal_pos }} |   R    |       1,010        |   -   |  -   |
{% endcapture %}

 -->


<!-- {% include en/dxl/control_table_return_delay_time.md %} -->

<!-- {% assign pages=site.pages | where:"ref", page.ref | sort: 'lang' %} -->

<!--

{% for reference in page.tab_ref %}

{{ reference }}

{% assign new_ref = reference %}

{% endfor %}

{{ new_ref.ref1 }}

-->

<!-- 테스트 끝  -->

<section id="{{ page.tab_title1 }}" class="tab_contents">

{% include en/dxl/x/xl430_w250.md %}

</section>

<section id="{{ page.tab_title2 }}" class="tab_contents">

{% include en/dxl/x/xc430_w150.md %}

</section>

<section id="{{ page.tab_title3 }}" class="tab_contents">

{% include en/dxl/x/xh430-w210.md %}

</section>

[xl430_new(pdf).pdf]: http://www.robotis.com/service/download.php?no=772
[xl430_new(dwg).dwg]: http://www.robotis.com/service/download.php?no=771
[xl430_new(stp).stp]: http://www.robotis.com/service/download.php?no=773
[xl430.pdf]: http://www.robotis.com/service/download.php?no=154
[xl430.dwg]: http://www.robotis.com/service/download.php?no=153
[xl430.stp]: http://www.robotis.com/service/download.php?no=155
[compatibility guide]: http://en.robotis.com/service/compatibility_table.php?cate=dx
[model number]: /docs/en/popup/x/model_number
[model information]: /docs/en/popup/x/
[firmware version]: /docs/en/popup/x/firmware_version
[protocol type]: /docs/en/popup/x/control_table_protocolversion
[id]: /docs/en/popup/x/control_table_id
[baud rate]: /docs/en/popup/x/control_table_baudrate_2
[return delay time]: /docs/en/popup/x/control_table_return_delay_time
[drive mode]: /docs/en/popup/x/control_table_drivemode
[operating mode]: /docs/en/popup/x/control_table_mx_opmode_2
[secondary(shadow) id]: /docs/en/popup/x/control_table_shadowid
[protocol type]: /docs/en/popup/x/control_table_protocolversion
[homing offset]: /docs/en/popup/x/control_table_homingoffset
[moving threshold]: /docs/en/popup/x/control_table_movingthreshold
[temperature limit]: /docs/en/popup/x/control_table_temp_limit_2
[max voltage limit]: /docs/en/popup/x/contron_table_max_min_voltage_level
[min voltage limit]: /docs/en/popup/x/contron_table_max_min_voltage_level
[pwm limit]: /docs/en/popup/x/control_table_pwm_limit
[velocity limit]: /docs/en/popup/x/control_table_vellimit
[max position limit]: /docs/en/popup/x/control_table_min_max_position_limit
[min position limit]: /docs/en/popup/x/control_table_min_max_position_limit
[shutdown]: /docs/en/popup/x/control_table_shutdown
[torque enable]: /docs/en/popup/x/control_table_torque_enable
[profile velocity]: /docs/en/popup/x/control_table_profile_velocity
[present position(132)]: /docs/en/popup/x/control_table_present_position
[led]: /docs/en/popup/x/control_table_led
[status return level]: /docs/en/popup/x/control_table_status_return_lv
[registered instruction]: /docs/en/popup/x/control_table_reg_instruction
[hardware error status]: /docs/en/popup/x/control_table_hardware_error-status
[velocity i gain]: /docs/en/popup/x/control_table_velocity_pi_gain
[velocity p gain]: /docs/en/popup/x/control_table_velocity_pi_gain
[position d gain]: /docs/en/popup/x/control_table_position_pid_gain
[position i gain]: /docs/en/popup/x/control_table_position_pid_gain
[position p gain]: /docs/en/popup/x/control_table_position_pid_gain
[feedforward 2nd gain]: /docs/en/popup/x/control_table_position_pid_gain
[feedforward 1st gain]: /docs/en/popup/x/control_table_position_pid_gain
[bus watchdog]: /docs/en/popup/x/control_table_buswatchdog
[goal pwm]: /docs/en/popup/x/control_table_goal_pwm
[goal velocity]: /docs/en/popup/x/control_table_goal_velocity
[profile acceleration]: /docs/en/popup/x/control_table_profile_acceleration
[profile velocity]: /docs/en/popup/x/control_table_profile_velocity
[goal position]: /docs/en/popup/x/control_table_goal_position_2
[realtime tick]: /docs/en/popup/x/control_table_realtime_tick
[moving]: /docs/en/popup/x/control_table_moving_2
[moving status]: /docs/en/popup/x/control_table_moving_status
[present pwm]: /docs/en/popup/x/control_table_present_pwm
[present load]: /docs/en/popup/x/control_table_present_load_2
[present velocity]: /docs/en/popup/x/control_table_present_velocity
[present position]: /docs/en/popup/x/control_table_present_position
[velocity trajectory]: /docs/en/popup/x/control_table_velocity_trajectory
[position trajectory]: /docs/en/popup/x/control_table_position_trajectory
[present input voltage]: /docs/en/popup/x/control_table_present_volt_2
[present temperature]: /docs/en/popup/x/control_table_present_temp_2
[indirect address 1]: /docs/en/popup/x/control_table_indirect_data
[indirect address 2]: /docs/en/popup/x/control_table_indirect_data
[indirect address 3]: /docs/en/popup/x/control_table_indirect_data
[indirect address 26]: /docs/en/popup/x/control_table_indirect_data
[indirect address 27]: /docs/en/popup/x/control_table_indirect_data
[indirect address 28]: /docs/en/popup/x/control_table_indirect_data
[indirect data 1]: /docs/en/popup/x/control_table_indirect_data
[indirect data 2]: /docs/en/popup/x/control_table_indirect_data
[indirect data 3]: /docs/en/popup/x/control_table_indirect_data
[indirect data 26]: /docs/en/popup/x/control_table_indirect_data
[indirect data 27]: /docs/en/popup/x/control_table_indirect_data
[indirect data 28]: /docs/en/popup/x/control_table_indirect_data
[indirect address 29]: /docs/en/popup/x/control_table_indirect_data
[indirect address 30]: /docs/en/popup/x/control_table_indirect_data
[indirect address 31]: /docs/en/popup/x/control_table_indirect_data`
[indirect address 54]: /docs/en/popup/x/control_table_indirect_data
[indirect address 55]: /docs/en/popup/x/control_table_indirect_data
[indirect address 56]: /docs/en/popup/x/control_table_indirect_data
[indirect data 29]: /docs/en/popup/x/control_table_indirect_data
[indirect data 30]: /docs/en/popup/x/control_table_indirect_data
[indirect data 31]: /docs/en/popup/x/control_table_indirect_data
[indirect data 54]: /docs/en/popup/x/control_table_indirect_data
[indirect data 55]: /docs/en/popup/x/control_table_indirect_data
[indirect data 56]: /docs/en/popup/x/control_table_indirect_data

{% include en/dxl/common_link.md %}
