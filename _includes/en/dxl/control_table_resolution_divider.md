It allows the user to change DYNAMIXEL’s resolution.  
The default Resolution Divider Value is set as 1. (1 ~ 4 available)  
When resolution is lowered, revolutions (in both directions) can be increased (up to 28 turns in each direction).  

```
Present Position = Real Position / Resolution Divider
```

For example, a Real Position of 2048 with a Resolution Divider set as 2 will yield a Present Position value of 1024 (2048/2 = 1024).  
A DYNAMIXEL with Resolution Divider set as 2 will have a resolution 2048 for a single revolution.  
The Present Position can be obtained while Multi-turn Offset and Resolution Divider are taken into account.  

```
Present position = (Real Position / Resolution Divider) + Multi-turn Offset
```

For example, a DYNAMIXEL with a Real Position of 2048 with a Resolution Divider set as 4 and Multi-turn Offset as 1024 will yield a Present Position of 1535 ((2048/4) + 1024 = 1535).

![](/assets/images/dxl/mx/mx-12_res_divider.jpg)

**NOTE** : This feature is only applied in multi-turn mode and will be ignored in other modes.
{: .notice}
