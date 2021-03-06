---
title: "Using Tang's GPIO"
date: 2019-02-15T20:14:28+05:30
weight: 5
draft: false
---

## Create a new project

In the Menubar goto **Project -> New Project** or use the shortcut key **Ctrl+Alt+P**.

Select **Device Family** and **Device Name** for Lichee Tang as shown below.

![New Project](/using-tang/using-gpio/images/a.png "New Project")

## Create a new HDL source file.

Right click on **Hierarchy** and click on **New Source** to make new HDL source file.

![O](/using-tang/using-gpio/images/b.png "O")

Select the HDL **File Type** and put source **File Name**. Check **Add To Project** to add this file to your project.

![O](/using-tang/using-gpio/images/c.png "O")

Copy the following code into text editor and save it, as shown in following image.

```toml
module gpio_main
	(
		input wire RST_N,
		output wire R_LED	
	);

assign R_LED = RST_N;

endmodule
```

![O](/using-tang/using-gpio/images/d.png "O")

Now we need to assign physical Pins to our IO ports. Double click on **IO Constraint** to open IO Constraint Dialog.

![O](/using-tang/using-gpio/images/e.png "O")

Select the **IO Bank** and **Pin Location** for Tang's onboard LED and Button then save it as adc file in the project.

![O](/using-tang/using-gpio/images/f.png "O")
![O](/using-tang/using-gpio/images/g.png "O")

Click on **Run** Icon to start compilation process.

![O](/using-tang/using-gpio/images/h.png "O")

Plug in you Lichee Tang board to USB and click on **Download** icon to open Download Dialog. 

![Open Download box](/getting-started/Getting-to-Blinky/images/d1.jpg "Open Download box")

Make sure your device detacted by TD IDE. Add generated bitstream file by clicking on **Add** button. Click on **Run** button to start Download process.

![O](/using-tang/using-gpio/images/i.png "O")

Download the Bitstream into SPI Flash to make your design run after power reset. 

![O](/using-tang/using-gpio/images/j.png "O")