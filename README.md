# Conky
Conky is a system monitoring tool that generates an output of various information related to your computer's hardware, system processes, and network activity. To use Conky, you will need to create a configuration file (".conkyrc") that contains a set of parameters that determine what information is displayed and how it is displayed.

## Design
The Conky display is aligned to the top right corner of the screen and includes graphical elements such as a battery bar, memory bar, and file system bars for root and swap partitions.

The SYSTEM and Uptime declarations display the system name, kernel version, and uptime, while the Battery declaration displays a battery status bar. The CPU Cores declaration displays a horizontal bar graph for each CPU core, indicating CPU usage.

The RAM declaration displays memory usage as a bar graph, and the STORAGE declaration displays storage usage for the root partition and swap partition as bar graphs. The TOP PROCESSES declaration displays the top five processes consuming memory.

The NETWORK declaration displays network activity for Ethernet, WiFi, and USB tethering if available. It includes the upload and download speeds and total upload and download data transfer. The if_existing statements check for the existence of the network interfaces before displaying their status.

## This is a Conky configuration file (`.conkyrc`) that displays various system information on the desktop.
The design elements and explanations are as follows:

## Window / Display declarations

### own_window
- `yes`: This option enables the window.
- `own_window_type desktop`: Specifies that Conky should be treated as a desktop window.
- `own_window_transparent no`: This option disables transparency.
- `own_window_argb_visual yes`: Specifies that an ARGB visual should be used.
- `own_window_argb_value 145`: Sets the alpha value for the window to 145.
- `own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager`: Defines the window hints. The window should be undecorated (i.e., without borders), below other windows, sticky (i.e., always visible), and not show up in the taskbar or pager.

### double_buffer
- `yes`: Enables double buffering. This makes the window flicker-free.

### minimum_size, maximum_width
- `minimum_size 200`: Sets the minimum width and height for the window to 200 pixels.
- `maximum_width 400`: Sets the maximum width for the window to 400 pixels.

### alignment
- `top_right`: Aligns the window to the top right corner of the desktop.

### gap_x, gap_y
- `gap_x 12`: Sets the horizontal gap between the window and the right edge of the screen to 12 pixels.
- `gap_y 40`: Sets the vertical gap between the window and the top edge of the screen to 40 pixels.

## Text / decoration

### use_xft
- `yes`: Enables XFT (X FreeType) font rendering. This allows the use of anti-aliased fonts.

#### xftfont
- `Source Code Pro:size=7`: Sets the font to "Source Code Pro" with a size of 7.

### The actual output

* SYSTEM
Displays the system name, kernel version, and machine type.

* Uptime
Displays the system uptime.

* Battery
Displays the battery status using a battery bar. The battery status is obtained from `BAT0`.

* CPU Cores
Displays the CPU usage for each core using a CPU bar.

* RAM
Displays the RAM usage using a RAM bar and text.

* STORAGE
Displays the storage usage for the root and swap partitions using bar graphs and text.

* TOP PROCESSES
Displays the top 5 processes in terms of memory usage.

* NETWORK
Displays the network information for Ethernet, WiFi, and USB tethering (if available) using bar graphs and text.

## Note
The network section uses variables that are specific to the system. If these variables are not defined, the section will not appear in the Conky output.

---
This Conky configuration file is designed for personal use and may require modification to work on other systems.

## License

This script is released under the [MIT License](LICENSE).
