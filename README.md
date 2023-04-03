# .conkyrc

# Conky is a system monitoring tool
Conky is a system monitoring tool that generates an output of various information related to your computer's hardware, system processes, and network activity. To use Conky, you will need to create a configuration file (".conkyrc") that contains a set of parameters that determine what information is displayed and how it is displayed.

# Design
The Conky display is aligned to the top right corner of the screen and includes graphical elements such as a battery bar, memory bar, and file system bars for root and swap partitions. The display is also transparent and has an opacity value of 145.

The configuration file contains several sections that define the appearance and content of the Conky output. The first section, Window/Display Declarations, defines the window properties, such as the type of window, transparency, and positioning. The double_buffer setting enables smooth animation and eliminates flickering.

The Text/Decoration section enables Conky to use TrueType fonts, and the xftfont parameter defines the font and size used in the output. The alignment setting determines the position of the Conky display on the screen, and the gap_x and gap_y settings define the horizontal and vertical spacing between the Conky display and the screen edge.

The SYSTEM and Uptime declarations display the system name, kernel version, and uptime, while the Battery declaration displays a battery status bar. The CPU Cores declaration displays a horizontal bar graph for each CPU core, indicating CPU usage.

The RAM declaration displays memory usage as a bar graph, and the STORAGE declaration displays storage usage for the root partition and swap partition as bar graphs. The TOP PROCESSES declaration displays the top five processes consuming memory.

The NETWORK declaration displays network activity for Ethernet, WiFi, and USB tethering if available. It includes the upload and download speeds and total upload and download data transfer. The if_existing statements check for the existence of the network interfaces before displaying their status.
