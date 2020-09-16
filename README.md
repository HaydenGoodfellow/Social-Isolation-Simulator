# Social-Isolation-Simulator
This project graphically simulates the effect of social isolation on the spread of a contagious disease by allowing users to control the percentage of people socially isolating.

It was created to work with the ARM Cortex-A9 processor on the DE1-SoC board. Accomplishing this required the implementation of our own PS/2 keyboard driver and VGA display driver. We utilized page-flipping and optimized code to ensure the animation of the simulation was smooth and free of screen-tearing.

Please note: Due to the COVID-19 shutdown of in-person labs, this project had to be able to run on an [online ARM Cortex-A9 simulator](https://cpulator.01xz.net/?sys=arm-de1soc). Consequently, it had to be written entirely in one file as the simulator does not support linking files. Normally I would have written this project modularly in multiple files with clear file names to improve code readability.

# Features:

## Graphics:
![Start Screen](https://github.com/HaydenGoodfellow/Social-Isolation-Simulator/blob/master/Images/StartScreenResized.png)

The graphics were created to work on the 320x240 VGA display and the program had to draw every pixel directly to the VGA buffers. Page-flipping was utilized to ensure the animations ran smooothly and were free of any screen-tearing. Multiple layers of abstraction, starting with drawing a single pixel, were created to ensure the code was clean and easy to read (as shown below). 

![Graphics Example](https://github.com/HaydenGoodfellow/Social-Isolation-Simulator/blob/master/Images/GraphicsExample.gif)

![Graphics Functions](https://github.com/HaydenGoodfellow/Social-Isolation-Simulator/blob/master/Images/GraphicsFunctions.png)

## Real-Time Statistics
Users are able to see a real-time graph showing the progression of the disease. The number of infected is shown using the red line, the number of recovered is shown using the blue line, and the number of deceased is shown using the white line. 

![Real Time Stats](https://github.com/HaydenGoodfellow/Social-Isolation-Simulator/blob/master/Images/RealTimeStatsResized.png)

Finally, at the end of the simulation, users are presented with the final statistics regarding their simulation.

![End Screen Stats](https://github.com/HaydenGoodfellow/Social-Isolation-Simulator/blob/master/Images/EndScreen.png)

## Complete User Customization
Users are able to tweak every key variable in the simulation including length of simulation, average recovery time, infection chance, number of people, number of initial infected, and number of people socially isolating. Additionally, users are also able to scale the screen resolution to the size of their own screen.

![Settings](https://github.com/HaydenGoodfellow/Social-Isolation-Simulator/blob/master/Images/Settings.png)
