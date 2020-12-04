{% capture dxl_led_policy %}  
**NOTE** : Check the status of DYNAMIXEL by the counts of flickering LED. 

|      Status      |  LED Representation  |
|:----------------:|:--------------------:|
|     Booting      |  LED flickers once   |
|   Factory Reset  | LED flickers 4 times |
|      Alarm       |     LED flickers     |{% if page.product_group=='dxl_x540' or page.ref=='mx-106-2' or page.ref=='mx-106' %}
|   Slave Mode     | LED flickers 3 times |{% else %}{% endif %}
|    Boot Mode     |        LED On        |

{% endcapture %}
<div class="notice">{{ dxl_led_policy | markdownify }}</div>
