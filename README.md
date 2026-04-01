# PREREQUISITES, HOW TO USE, AND INSTALLATION
 
## Prerequisites
 
### Robot Hardware
- Tank-drive chassis (no X-drive, H-drive, or mecanum)
- All chassis wheels must be the same size
- Clear left/right motor split for the chassis
- VEX V5 inertial sensor
- V5 motors only
- Single controller only
 
### Software
- VEX VS Code extension (PROS is not supported)
- V5 platform only (IQ and EXP are not supported)

First download the VEXLearn Guide.pdf. The PDF file contains the instructions on how to download, setup, and use the template. Please follow the instructions in the setup guide carefully to avoid any issues. If you encounter any issues or found a bug, please report it to me via the "Issues" tab on the top left, your feedback is hugely appreciated.

---

# VEXLearn-Template
VEXLearn is not a competition-focused template. It is a **teaching template**, its goal is to help users understand how VEX software works from the ground up. Every file in the template is documented with introductions, structure explanations, inline comments, and troubleshooting Q&As so that users can learn by reading and modifying real code.
 
If you are looking for a competition-ready template with odometry and coordinate systems, consider [JAR Template](https://github.com/JacksonAreaRobotics/JAR-Template) or [LemLib](https://github.com/LemLib/LemLib). VEXLearn is a stepping stone, once you understand the fundamentals here, using JAR Template or LemLib becomes much easier.

---

## Notes for Users
 
- The PDF guide is the companion to this template, read it alongside the code
- Every file has a troubleshooting section at the bottom covering the most common issues
- If your problem isn't covered, open a GitHub issue and I will respond
- For skills autonomous or more reliable / powerful templates, switch to JAR Template or LemLib, they support odometry which is essential for more advanced robots.
- Run-to-run variation is normal. Tune between matches. Always keep your battery above 75% when tuning

---
 
## Features
 
- **Tank drive chassis control** with deadband, coast-to-brake timing, and sensitivity tuning
- **Voltage-based PID movement functions** (`move` and `turn`) with heading correction, exit voltage chaining, and integral windup prevention
- **RPM-based movement functions** (`moveRPM` and `turnRPM`) included for reference, though voltage control is recommended
- **Multi-screen Brain display** with a menu, motor diagnostics, battery info, team info, and software info screens, all touch-navigable
- **Controller display** showing heading, average motor temperature, and battery percentage
- **Autonomous function templates** for BlueRight, BlueLeft, RedRight, RedLeft, and Skills
- **Full PDF guide** covering setup, C++ fundamentals, VEX concepts, PID tuning, and tips from real competition experience
- **Troubleshooting sections** in every file addressing the most common beginner mistakes

---
 
## File Structure
 
```
project/
├── include/
│   ├── auto.h          # Autonomous function declarations
│   ├── display.h       # Brain and controller display function declarations
│   ├── drive.h         # Drive function declaration
│   ├── movement.h      # Movement function declarations
│   ├── robotConfig.h   # Hardware extern declarations
│   └── vex.h           # VEX SDK header + wheel_2r definition
└── src/
    ├── auto.cpp        # Autonomous functions (write your routes here)
    ├── display.cpp     # Brain and controller display logic
    ├── drive.cpp       # Driver control function
    ├── main.cpp        # Pre-auton, autonomous, and usercontrol entry points
    ├── movement.cpp    # PID movement functions
    └── robotConfig.cpp # Hardware initialization
```
 
---
