The Home Offset(20) adjusts the home position. The offest value is added to the [Present Position(132)].  

**Present Position(132) = Actual Position + Homing Offset(20)**

|        Unit         |                  Value Range                  |   Description    |
|:-------------------:|:---------------------------------------------:|:----------------:|
| about 0.088 [&deg;] | -1,044,479 ~ 1,044,479<br />(-255 ~ 255[rev]) | 4,096 resolution |

**NOTE** : In case of the Position Control Mode(Joint Mode) that rotates less than 360 degrees, any invalid Homing Offset(20) values will be ignored(valid range : -1,024 ~ 1,024).
{: .notice}

**NOTE** : In the case of Reverse Mode bit is set in [Drive Mode(10)](#drive-mode10), the sign of Homing Offset(20) value will not be reversed.
{: .notice}
