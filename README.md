# iit-inail-drill-ros-pkg

Descriptions for HHCM, IIT's drill actuator



### Usage
Add the gripper to the robot with the provided macro:
```xml
  <xacro:include filename="$(find inail_drill_urdf)/urdf/inail_drill_macro.urdf.xacro" />
  
  <link name="world"/>
  
  <xacro:inail_drill parent_link="world">
    <origin xyz="0 0 0" rpy="0 0 0"/>
  </xacro:inail_drill>

```
