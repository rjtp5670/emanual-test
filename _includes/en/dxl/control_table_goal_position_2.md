{% assign passed_product_group = include.passed_ref %}
{% assign passed_model = include.passing_model %}

- Passed Ref: {{ passed_product_group }}
- Passed Model: {{ passed_model }}


# Goal Position
The Goal Position(116) sets desired position.  From the front view of DYNAMIXEL, CCW is an increasing direction, whereas CW is a decreasing direction. The way to reaching the Goal Position(116) differs by 4 Profiles provided by DYNAMIXEL. See the [What is the Profile] for more details.

![](/assets/images/dxl/x/dxl_goal_position.jpg)

| Mode     | Values     | Description |
| :--------: | :--------: | :--------: |
| Position Control Mode | Min Position Limit(52) ~ Max Position Limit(48)| Initial Value : 0 ~ 4,095|
|Extended Position Control Mode|-1,048,575 ~ 1,048,575|-256[rev] ~ 256[rev]|{% if passed_product_group!='dxl_xl430' and passed_model!='mx-28-2' %}
|Current-based Position Control Mode|-1,048,575 ~ 1,048,575|-256[rev] ~ 256[rev]|{% else %}{% endif %}

|Degree Conversion Constant|Description|
| :---: | :---: |
|0.088&deg;/Value| 1[rev] : 0 ~ 4,095 |


{% capture notice_01 %}
**NOTE** : The [Profile Velocity(112)](#profile-velocity-{{ passed_model }}){: .popup2} and the [Profile Acceleration(108)](#profile-acceleration-{{ passed_model }}){: .popup2} are applied in below cases.
- When the [Operating Mode(11)](#operating-mode-{{ passed_model }}){: .popup2} is **Position Control Mode**, the Profile Velocity(112) and the Profile Acceleration(108) are used to create a new profile if the Goal Position(116) is updated.
- When the Operating Mode(11) is **Velocity Control Mode**, the Profile Acceleration(108) is used to create a new profile if [Goal Velocity(104)](#goal-velocity104) is updated.
{% endcapture %}
<div class="notice">{{ notice_01 | markdownify }}</div>

**NOTE** : When turning off the power supply or changing Operation Mode on Extended Position Control Mode, the value of Present Position is reset to the absolute position value of single turn .
{: .notice}

{% include en/dxl/control_table_opmode_note.md %}
