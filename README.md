## .conkyrc
A Conky configuration file, also known as a `.conkyrc` file, is a text file that controls the appearance and behavior of the Conky system monitoring tool. It contains various settings and parameters that dictate what information should be displayed, where it should be displayed, and how it should be formatted.

The .conkyrc file is highly customizable and can be edited to suit individual preferences. It supports a wide range of built-in variables and commands that allow users to display system statistics such as CPU usage, memory usage, disk usage, network traffic, and more.

In addition to the above, users can create their own custom scripts and commands to display additional information or perform specific actions.

---

## Included file
I provided my .conkyrc file from my production machine. It contains all the pertinent information most users will find to suit their daily needs.

Conky is set to update information every 1 second. Users may modify this interval by changing the value in the `update_interval` section. A shorter interval may increase system resource usage, while a longer interval may not display real-time information.

The display is aligned to the top-right corner of the screen. Users may modify the positioning by changing the values in the `alignment` and `gap_x`/`gap_y` sections. It includes graphical elements to suppliment text.

### This implementation displays
- system name
- kernel version
- uptime
- battery status
- CPU use bar graphs
- memory usage bar graph
- root and swap partitions usage bar graphs
- the top five processes
- network interface information

#### Networking
Information for specific network interfaces, in my case, `wlan0` is displayed.
> **Users may need to modify these interface names if their system has different interface names.**

It displays network activity for Ethernet, WiFi, and USB tethering, **if available**. It includes the upload and download speeds and total upload and download data transfer. The `if_existing` statements check for the existence of the network interfaces before displaying their status.

---

## Screenshot
![Screenshot_2024-10-24_10-37-13](https://github.com/user-attachments/assets/a618f96d-e86d-4ce1-877f-684a57cb31f9)


## Elements:

### Window / Display declarations

#### own_window
- `own_window yes`: This option enables the window.
- `own_window_type desktop`: Specifies that Conky should be treated as a desktop window.
- `own_window_transparent yes`: This option enables transparency.
- `own_window_argb_visual yes`: Specifies that an ARGB visual should be used.
- `own_window_argb_value 145`: Sets the alpha value for the window to 145.
- `own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager`: Defines the window hints. The window should be undecorated (i.e., without borders), below other windows, sticky (i.e., always visible), and not show up in the taskbar or pager.

#### double_buffer
- `yes`: Enables double buffering. This makes the window flicker-free.

#### minimum_size, maximum_width
- `minimum_size 200`: Sets the minimum width and height for the window to 200 pixels.
- `maximum_width 400`: Sets the maximum width for the window to 400 pixels.

#### alignment
- `top_right`: Aligns the window to the top right corner of the desktop.

#### gap_x, gap_y
- `gap_x 52`: Sets the horizontal gap between the window and the right edge of the screen to 12 pixels.
- `gap_y 12`: Sets the vertical gap between the window and the top edge of the screen to 12 pixels.

### Text / decoration

#### use_xft
- `yes`: Enables XFT (X FreeType) font rendering. This allows the use of anti-aliased fonts.

#### xftfont
- `Source Code Pro:size=7.5`: Sets the font to "Source Code Pro" with a size of 7.5.
#### color
- `color1 FFFFFF`: WHITE, represented as a hex value.
---

## Note
The font and color choices in the file may not suit everyone's preferences. Users can modify the font and color settings to match their taste by changing the values in the corresponding sections.

The network section uses variables that are specific to the system. If these variables are not defined, the section will not appear in the Conky output, as this Conky configuration file was designed for my personal use. It may require modification to work on other systems.

---

## 🤪 Conky Meta

- [888v](https://github.com/apple-fritter/888v): Virtual webcam clone with Conky overlay; Bash.
- [.conkyrc](https://github.com/apple-fritter/.conkyrc): conky configuration file.
- [moonphase.py](https://github.com/apple-fritter/conky.moonphase.py): RSS reader for Conky that reads in a TSV based list of feeds. Python.
- [RTSP-view.py](https://github.com/apple-fritter/conky.RTSP-view.py): Script that displays an RTSP stream. Python.
- [tide.py](https://github.com/apple-fritter/conky.tide.py): Script that displays the local tide using the Tidal API. Python.
- [twitter.py](https://github.com/apple-fritter/conky.twitter.py): Script that displays a user's Twitter notifications. Python.

---

## [Disclaimer](DISCLAIMER)
**This software is provided "as is" and without warranty of any kind**, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.

**The authors do not endorse or support any harmful or malicious activities** that may be carried out with the software. It is the user's responsibility to ensure that their use of the software complies with all applicable laws and regulations.

---

## License

These files released under the [MIT License](LICENSE).
