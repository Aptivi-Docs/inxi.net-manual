---
description: Graphics Processing Unit (GPU)
---

# 🖼 Graphics

This lists information about the graphics cards that are parsed by Inxi. You can use the below properties to learn more about its information.

Module name according to each operating system:

| OS      | Module name             |
| ------- | ----------------------- |
| Linux   | `004#Graphics`          |
| Windows | `Win32_VideoController` |

You can call the module either by enumerating through the entire dictionary of the graphics cards, or you can use the graphics card name directly as follows:

```csharp
HardwareInfo.GPU["NVIDIA GeForce RTX 3080 SUPER"].<property>
```

which `<property>` is:

| Property      | Type   | Description         |
| ------------- | ------ | ------------------- |
| Name          | String | Graphics card name  |
| Driver        | String | Driver used         |
| DriverVersion | String | Driver version used |
| BusID         | String | Device Bus ID       |
| ChipID        | String | Device ID           |

{% hint style="warning" %}
Device bus ID is not supported yet on Windows.
{% endhint %}
