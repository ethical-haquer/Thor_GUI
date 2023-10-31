
# Thor GUI

A GUI for the [Thor Flash Utility](https://github.com/Samsung-Loki/Thor).

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/5e180060-1595-44fa-91af-e261586c24c0">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/b97628ef-a932-4ef3-8bdf-cc3005895a83">
  <img alt="Screenshot of Thor GUI">
</picture>
<details>
  <summary><b>Screenshots</b></summary>
  <br>
  <b>NOTE:</b> This section is a work-in-progress
  <br>
  <br>
  "Options" Tab:
  <br>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/ab9d9c64-5230-4d14-8186-8f41fc7b33e9">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/e2f51f25-e682-48f9-97ad-0f8d189ca460">
    <img alt="Options Tab">
  </picture>
  <br>
  Command Entry:
  <br>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/7d875fc7-bead-47bd-943c-d3622b320546">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/136b84a6-81f8-4ed9-b7e2-1e2ebfc973ff">
    <img alt="Command Entry">
  </picture>
  <br>
  "Connect Device" Window:
  <br>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/d4574054-5f7f-4c8a-9d4c-4de41c3690fd">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/d4574054-5f7f-4c8a-9d4c-4de41c3690fd">
    <img alt="Connect Device Window">
  </picture>
  <br>
  "Select Partitions" Window:
  <br>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/620d05e8-872e-44d7-946e-fca7bf80e311">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/83a61e3c-09d7-41a5-8178-124abc6fc623">
    <img alt="Select Partitions Window">
  </picture>
  <br>
  "Verify Flash" Window:
  <br>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/7d3d6e6c-af3c-48eb-bd31-263741b3f5b7">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/ethical-haquer/Thor_GUI/assets/141518185/48a7da84-1474-4d09-9b9d-ae2a74d02100">
    <img alt="Verify Flash Window">
  </picture>
</details>

## Intro

After witnessing a new Linux user, who had just switched over from Windows, struggle with using Odin4's CLI, I decided to try and make a GUI for the Thor Flash Utility. If you aren't comfortable with the command line, or just prefer a GUI, then this could be helpful for you. On the other hand, if you are comfortable using the command line, then you may just want to use Thor in the terminal. And yes, this is my first GitHub project, so please let me know if you have any suggestions. :slightly_smiling_face:

## Disclaimer

Currently, Thor GUI is in an Alpha stage. Not all of Thor's features have been implemented in the GUI, and there are known (and probably unknown) bugs. A list of missing features and know bugs in the **latest release** can be found below.

## Known Bugs

In addition to [Thor's own issues](https://github.com/Samsung-Loki/Thor/issues), here are Thor GUI's:

Functional:
+ Currently, the only interactive Thor commands (ones that require user input, such as "flashFile") that can be used are "connect" and "flashTar". This doesn't affect non-interactive Thor commands that don't require input, such as "help", "begin odin", etc.
+ Using the dark theme on X11, the file picker text is white, a well as the background. This is a [known Sun Valley issue](https://github.com/rdbende/Sun-Valley-ttk-theme/issues/104). The work-around is to click and drag the pointer over the files and diectories displayed, which will turn them blue, and therefore readable.

Aesthetic:
+ The output from interactive commands (ones that require user input, such as flashTar, connect, etc.) is echoed. So if Thor outputs interactive text, it will be displayed two times. Also, when Thor GUI sends Thor keypresses to select things and such, Thor will send the new output, also echoed. Like when a "[ ]" changes to a "[X]", that whole section of output will be displayed again.

## Implemented Thor features

- [x] Connecting/Disconnecting devices
- [x] Starting/Stopping an Odin session
- [x] Setting options
- [x] Typing and sending Thor a command
- [x] Flashing Odin archives
- [ ] Flashing a single partition
- [ ] Printing a description of a device's partition table
- [ ] Dumping a device's partition table into a PIT file
- [ ] Printing a description of any PIT file

## Planned improvements

+ A more extensive Settings

## Prerequisites

### Pexpect

```
pip install pexpect
```

### Sun Valley ttk theme

```
pip install sv-ttk
```

### tkinter-tooltip

```
pip install tkinter-tooltip
```

### tkinterDnD

'''
pip install python-tkdnd
'''

## Installation

+ First, make sure you have the above prerequisites.
+ Download the latest Thor GUI release from [here](https://github.com/ethical-haquer/Thor_GUI/releases).
+ Once it's downloaded, extract it.
+ Then run:

  ```
  python3 PATH/TO/Thor_GUI.py
  ```
+ If a sweet-looking GUI shows up, then you've finished installing Thor GUI!

> [!NOTE]
> If you encounter any issues, or have any questions, just let me know and I'll be glad to help. 🙂

## Usage
**NOTE:** This section is a work-in-progress

https://github.com/ethical-haquer/Thor_GUI/assets/141518185/5df866bb-74d1-40ba-b5b0-571ed88d68a3

<details>
  <summary><b>Guide</b></summary>
  <br>
  <b>Starting Thor (0:00):</b>
  <br>
  To start Thor, click the "Start Thor" button. This is usually the first thing you'd do after running Thor GUI.
  <br>
  <br>
  <b>Connecting to a device (0:09):</b> 
  <br>
  To connect to a device, click the "Connect" button. A pop-up window will appear, asking you what device you'd like to connect to. Choose a device, and then click "Select".
  <br>
  <br>
  <b>Starting an Odin protocol (0:17):</b>
  <br>
  To start an Odin protocol, which is needed to flash a device, click the "Start Odin protocol" button. 
  <br>
  <b>Fun fact:</b> The top three buttons in Thor GUI are placed in the order they should be used, from left to right.
  <br>
  <br>
  <b>Flashing Odin archives (0:19)</b> 
  <br>
  To flash Odin archives, first select what files to flash. You may either select the files with a file picker, by clicking one of the file buttons (For example, to select a BL file, click the "BL" button), or type the file path into the corresponding entry. Only files which are selected with the check-boxes will be flashed. 
  <br>
  <br>
  To flash the selected files, hit the "Start" button. There are a few requirements that must be met for it to start the flash: 
  <br>
  At least one file must be selected (with the check-boxes), 
  <br>
  All selected files must exist, 
  <br>
  All selected files must be a .tar, .md5, or .zip, 
  <br>
  All selected files must be in the same directory. 
  <br>
  <br>
  If any of these above conditions is not met, Thor GUI will simply let you know, so don't worry.
  <br>
  <br>
  After a flash has been started, you will be presented with a "Select Partitions" Window. You may click "Select All" to select all of the listed partitions, or choose certain partitions to flash. Once you have finished selecting the partitions you want to flash, hit the "Select" button. There will be a "Select Partitions" Window for <b>every file</b> you selected with the check-boxes.
  <br>
  <br>
  After you have finished selecting partitions to flash you will see a "Verify Flash" window. This is your chance to cancel the flash if needed, by clicking the "No" button. Otherwise, click the "Yes" button and the flash will start.
  <br>
  <br>
  <b>Running a <a href="https://github.com/Samsung-Loki/Thor#current-list-of-commands">Thor command</a> (1:12):</b> 
  <br>
  To send Thor a command, enter it into the Command Entry (upper-right corner of Thor GUI, under the "Start Thor" button) and hit Enter. (the key on the keyboard, not the button on Thor GUI)
</details>

## How you can help

Here are some ways you can help me improve/finish Thor GUI:
+ Find and report bugs. If you find an issue that isn't listed above in "Known Bugs", please let me know!
+ Improve the code. Pull requests are always welcome!

## Credits

[TheAirBlow](https://github.com/theairblow) for the [Thor Flash Utility](https://github.com/Samsung-Loki/Thor)

[rdbende](https://github.com/rdbende) for the [Sun Valley tkk theme](https://github.com/rdbende/Sun-Valley-ttk-theme)

Myself, [ethical_haquer](https://github.com/ethical-haquer), for Thor GUI

## License

Thor GUI is licensed under GPLv3. Please see [`LICENSE`](./LICENSE) for the full license text.
